# trimble-id
Trimble Identity SDK for Java

📚 [Documentation](#documentation) - 🚀 [Getting Started](#getting-started) - 💬 [Support](#support)

## <a name="documentation">Documentation</a>

- [Developer guide](https://github.com/trimble-oss/trimble-id-sdk-docs-for-java/blob/main/docs/DeveloperGuide.md) - Our Dev guide to work with authentication grant types and its providers.
- [Reference documentation](https://github.com/trimble-oss/trimble-id-sdk-docs-for-java/blob/main/reference-guide) - Our code reference documentation generated from code comments.
- [Samples](https://github.com/trimble-oss/trimble-id-sdk-docs-for-java/blob/main/samples) - a code guided samples for supporeted grant type token providers.
- [Release Notes](https://github.com/trimble-oss/trimble-id-sdk-docs-for-java/blob/main/release-notes/CHANGELOG.md) - release notes about trimble-id client library.

## <a name="getting-started">Getting Started</a>

### Installation

**Apache Maven**

```sh
<dependency>
    <groupId>com.trimble</groupId>
    <artifactId>trimble-id</artifactId>
    <version>1.0.0</version>
</dependency>
```

**Gradle**
```sh
implementation group: 'com.trimble', name: 'trimble-id', version: '1.0.0'
```

### Configure Trimble Identity

Create a new application in the [Trimble Developer Console](https://developer.console.trimble.com) portal and configure the following settings:

To register your application in Trimble Developer Console:

1. On the left pane select "Applications".

2. On the Applications home page, in the top right corner select + NEW APPLICATION. The Create Application page displays.

3. Select Continue to enter the applications details.

    | Field       | Description |
    | ----------- | ----------- |
    | Name        | Name of your application                    |
    | Description | Provide a description for the application.  |

4. Configure Grant Type and Token preferences of your application choice.

    | Field       | Description |
    | ----------- | ----------- |
    | Application Grant Types        | Select the grant types that will be used for authenticating users or applications.                    |
    | Allowed Callback URLS| Refers to the redirect URI of the application after logging into Identity. More than one URL can be added to this field. The total URI length should not exceed 400kb. This field appears only when you select the Authorization Grant type.  |
    | Allowed Logout URLS | The URIs that Identity can redirect to after log out. More than one UL can be added to this field. The total URI length should not exceed 400kb. This field appears only when you select the Authorization Grant type.  |

5. Select "Create Application" to save changes.

Take note of the Client ID and URLs under the "Basic Information" section. You'll need these values to configure the SDK.

**Scopes**

Trimble Identity uses scopes to determine the aud claim in the returned access token. Scope is mandatory for the application to work. You can use the scope as the application name registered in the Trimble Developer Console. For example, if you have registered an application with the name "test", then it must be registered in the format {some_uuid}-"test". For eg., 12345678-1234-1234-1234-123456789012-test.

For more information, see [Authentication documentation](https://developer.trimble.com/docs/authentication).

## Raise an issue

To provide feedback or report a bug, please [raise an issue on our issue tracker](https://github.com/trimble-oss/tcp-sdk-docs-for-java/issues).

## <a name="support">Support</a>

Send email to [support@trimble.com](mailto:support@trimble.com)
