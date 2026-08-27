# gRPC Client Worker Template

A Worker User Library template that connects a Workers for LabVIEW application to gRPC servers written in LabVIEW, Python, C++, or any other supported language.

The Worker wraps the NI generated gRPC code so that the rest of your application communicates with it through a Worker's Public API, i.e. its Public Requests and Responses. gRPC stays at the application boundary rather than leaking through the Worker hierarchy.

## Dependencies

**Install these before opening the project.** The template will not run without them.

Download [grpc-labview.zip](https://github.com/ni/grpc-labview/releases/download/v1.7.0.1/grpc-labview.zip) from the NI gRPC LabVIEW repository on GitHub and install the three VI packages it contains:

| VI package |
| --- |
| `ni_lib_labview_grpc_library-1.7.0.1.vip` |
| `ni_lib_labview_grpc_servicer-1.7.0.1.vip` |
| `ni_lib_grpc_server_and_client_template[2]-1.7.0.1.vip` |

LabVIEW 2019 or later is required.

## What is in the project

| Item | Purpose |
| --- | --- |
| `template.proto` | The Public API contract. The generated code on both ends derives from this file. |
| `Generated_client.lvlib` | NI gRPC generator output. |
| `gRPC Client (template.proto).lvlib` | gRPC Client Worker. Connects to the gRPC server and handles the bidirectional stream. |
| `gRPC Client Tester.lvclass` | Tester Worker. Calls the gRPC Client Worker and provides the front panel used to send and receive messages. |
| `Launcher - gRPC Client Tester.vi` | Launches the tester. |

## The contract

`template.proto` defines a single bidirectional stream carrying nine messages in each direction, `Msg_ToServer_1..9` and `Msg_ToClient_1..9`. Every message starts as a placeholder; you replace its fields with the payload your application needs.

The message names are frozen. The LabVIEW gRPC generator derives VI, typedef and class names from them, so keeping them fixed means the regenerated libraries drop into an existing Worker unchanged. The proto header lists exactly what must not be renamed:

- `package w4lvgrpc`
- `service Session` and `rpc Connect`
- `ToServer` / `ToClient` and their oneof cases `msg_1..msg_9`
- the message names `Msg_ToServer_1..9` / `Msg_ToClient_1..9`

Everything inside the numbered messages is yours to change, along with any supporting types you add and all comments.

## Running the tester

The tester is designed to be used together with the **gRPC Server Worker Template Tester**, or with a server application written in another programming language that implements the same `template.proto` contract.

1. Run **Launcher - gRPC Server Tester.vi** in the gRPC Server Worker Template project and press **Create gRPC Server**. Wait for the **Server Listening** LED.
2. Run **Launcher - gRPC Client Tester.vi** to launch the tester, then press **Create gRPC Client**. The **Client Connected** LED lights when the stream is open.
3. Enter text in any **Msg_ToServer** control to send a message to the server. Messages received from the server appear under their corresponding **Msg_ToClient** indicators.
4. Press **Destroy gRPC Client** when finished to close the stream and disconnect from the server.

The tester panel exposes five of the nine messages in each direction. The remaining messages exist in the contract and are available to your application.

## Adapting the template

Fill the free messages in `template.proto` with the payloads your application needs, regenerate the LabVIEW library, and replace it in your project. Because the frozen names are unchanged, everything else stays put.

For a full walk through of this process, including the code generation, see [Using the gRPC Worker Templates](https://community.workersforlabview.io/private-articles/post/using-the-grpc-worker-templates-nZFACBeQcmMJnXm).

## Notes

**Real-time targets are untested.** The NI gRPC library supports NI Linux RT with system image 2022 Q4 or later, but this template has not been verified on an RT target.

## Licence

BSD-0
