<img src="https://cuplink.net/img/logo.png" alt="CupLink Logo" style="height: 32px; vertical-align: middle; margin-right: 8px;"> **Tensor**
=================================================================================

**Your privacy, uncompromised** - Serverless, encrypted video and voice calling over RiV-mesh

**Tensor** offers a new paradigm in secure communication. It's completely serverless, fully encrypted, and effortlessly private. Built on **RiV-mesh™**, the decentralized IPv6 mesh network infrastructure, Tensor enables true peer-to-peer voice and video calling without accounts, servers, or surveillance.

## Two Components. One Seamless Experience.

**Tensor** is composed of two integrated layers:

### • Overlay Peer-to-peer Network
A resilient, decentralized connectivity layer powered by **RiV-mesh™**, enabling direct communication between devices without accounts or centralized control.

### • The Tensor App  
An intuitive, lightweight calling interface that lets you connect instantly in up to 4K+ resolution. It's encrypted end-to-end, key-based, and fully user-controlled.

Perfect for use in home networks, company LANs, community mesh setups, or fully offline scenarios. The application uses Android's VpnService framework to establish the mesh network environment for peer-to-peer communication.

* * *

### 🔐 Core Features

#### Communication Excellence
*   **Peer-to-peer voice and video calling** in ultra-high-definition (supported up to 4K+)
*   **End-to-end+ encryption** built directly into the network layer
*   **Push-to-talk** and speaker mode for flexible communication
*   **Call-spy detection** with intelligent real-time alerts and app boot protection
*   **Android Auto integration** for seamless vehicle communication

#### Privacy & Security
*   **No accounts, servers, or internet access required** - works in same LAN or offline
*   **Private key-based identity management** - no logins, no phone numbers
*   **Self-generated Virtual Static IPv6** addresses for secure identification
*   **Encrypted local backup** of contacts, calls, and settings using libsodium
*   **Zero data collection** - no tracking, no monetization of user data

#### Network Architecture
*   **RiV-mesh™ overlay network access** - decentralized IPv6 mesh infrastructure
*   **QR code based contact exchange** - scan-to-connect simplicity, no setup required
*   **Public peer discovery & auto-routing** using IPv6 multicast
*   **Wi-Fi Direct support** for direct local communication
*   **Self-organizing mesh topology** with automatic peer discovery
*   **Cryptographic IPv6 identities** for secure peer authentication

#### Technical Implementation
*   **Android VpnService framework** - creates secure mesh network overlay
*   **WebRTC protocols** for audio/video communication with built-in encryption
*   **libsodium encryption** for database and communication security
*   **Zero-configuration networking** - plug-and-play connectivity

* * *

### 📱 Supported Platforms

*   Android 5.0 (Lollipop) and up.
    
*   Android Auto (in-call mode).
    
*   Experimental builds for desktop coming soon.
    
*   Support for various mesh network environments including Wi-Fi Direct, IPv6 multicast, and local LAN setups.

* * *

### 🌐 Peer Architecture

Tensor acts as a full mesh node in the **RiV-mesh™** decentralized IPv6 overlay network. Each peer can route traffic for others, enabling scalable, serverless communication with the following architecture:

#### Decentralized Mesh Network
*   **Full mesh topology** - every Tensor device is a routing node
*   **Self-organizing network** - automatic peer discovery and connection management
*   **No central servers** - completely decentralized communication infrastructure
*   **IPv6 native overlay** - built on cryptographic IPv6 addressing

#### RiV-mesh™ Integration
*   **EUI-64 format addressing** - self-generated cryptographic IPv6 addresses
*   **Multicast peer discovery** - automatic discovery of nearby mesh nodes
*   **Mesh-based routing** - uses intermediate nodes for efficient packet forwarding
*   **Static IPv6 addressing** - predictable, secure network identification

#### Security Model
*   **Cryptographic peer authentication** - verified device identities
*   **End-to-end encryption** - secure communication at the network layer
*   **Zero-trust architecture** - no implicit trust, all connections verified
*   **Self-sovereign networking** - complete user control over network participation

* * *

### 📄 How It Works

Tensor operates through a sophisticated 7-step process that creates a completely decentralized communication environment:

#### Step-by-Step Process

1. **Application Installation** - User installs Tensor application on Android device
2. **VpnService Activation** - Application automatically starts MainService VpnService in background
3. **Mesh Network Establishment** - VpnService establishes connection using secure tunnel (RiV-mesh™)
4. **IPv6 Address Generation** - Self-generated Virtual Static IPv6 addresses are created and assigned to devices
5. **Overlay Network Routing** - Communication is routed through mesh overlay network without traditional internet infrastructure
6. **Contact Exchange** - Contacts are exchanged via QR codes or text blobs (scan-to-connect simplicity)
7. **Direct Call Establishment** - Calls are established directly using devices' self-generated IPv6 addresses

#### Technical Implementation

*   **QR Code Contact Exchange** - Devices exchange identity and address using QR codes (contact name + static IPv6)
*   **Direct RiV-mesh™ Connection** - Tensor connects directly using RiV-mesh™'s cryptographic overlay IPv6 network
*   **Multicast Peer Discovery** - Peer discovery happens via IPv6 multicast; fallback via public peer tables
*   **Sovereign Networking** - No DHCP or external DNS required—fully self-contained networking
*   **Zero-Configuration Setup** - No manual network configuration needed

#### Why This Matters

Most apps route your calls through corporate servers and monetize your identity. Tensor does the opposite by removing the server, removing the account, and returning control to you. No ads. No tracking. No compromises.

* * *

### 📦 Build Instructions

#### Prerequisites
*   **Android Studio** - Latest version with Android SDK
*   **Go 1.19+** - Required for building RiV-mesh™ infrastructure components
*   **Linux-based System** - Recommended for development environment

#### Development Setup
*   **Source Building** - Support for building from sources on Linux-based systems
*   **Android Studio Integration** - Full IDE support for Android development
*   **Maven Dependencies** - WebRTC library available through Maven repository
*   **Cross-platform Support** - Build for multiple Android versions and architectures

#### RiV-mesh™ Integration
*   **Mobile.Mesh Library** - Provides RiV-mesh (RiV-mesh™) infrastructure for peer-to-peer communication
*   **VpnService Framework** - Required for establishing mesh network environment
*   **IPv6 Overlay Network** - Built on RiV-mesh™ decentralized mesh infrastructure

#### Building RiV-mesh™ Infrastructure
To build the underlying RiV-mesh™ mesh network infrastructure:

1. **Install Go 1.19+** - Required for building RiV-mesh™ components
2. **Clone RiV-mesh™ Repository**:
   ```bash
   git clone https://github.com/RiV-chain/RiV-mesh.git
   cd RiV-mesh
   ```
3. **Build for Your Platform**:
   ```bash
   # Linux/macOS
   ./build
   
   # Windows
   go mod tidy
   go build -o mesh.exe ./cmd/mesh
   go build -o meshctl.exe ./cmd/meshctl
   go build -o genkeys.exe ./cmd/genkeys
   ```
4. **Generate Configuration**:
   ```bash
   ./mesh -genconf > mesh.conf
   ```

#### Android Development
For Android-specific development:

1. **Android Studio Setup** - Install latest Android Studio with Android SDK
2. **NDK Installation** - Required for native library compilation
3. **Gradle Configuration** - Ensure proper dependency management
4. **Emulator Testing** - Use Android emulator with VPN support for testing

#### Cross-Platform Building
*   **Linux**: Native build support with full feature set
*   **macOS**: Intel and Apple Silicon support
*   **Windows**: MSI installer generation and manual builds
*   **Android**: AAR bundle generation for mobile integration

### 📋 Google Play Compliance

*   Tensor uses Android's VpnService framework to create a secure mesh network environment called RiV-mesh™
*   This usage is compliant with Google Play's VpnService policy because it provides VPN as core functionality for peer-to-peer communication
*   No personal data collection or redirection of user traffic for monetization purposes
*   All data from device to VPN tunnel endpoint is encrypted end-to-end

### 📄 Licensing

**Tensor** is open source software developed by **RiV Chain™ Limited**:
- **License**: GNU General Public License v3.0 (GPLv3)
- **Platform**: Android with VpnService framework
- **Infrastructure**: Built on RiV-mesh™ mesh networking (LGPLv3)
- **Commercial Use**: Allowed with full GPLv3 compliance requirements
- **Source Code**: Available at [GitHub](https://github.com/RiV-chain/CupLink)

**RiV-mesh™ Infrastructure** (used by Tensor):
- **License**: GNU Lesser General Public License v3.0 (LGPLv3)
- **Scope**: All mesh networking functionality, REST API, protocol implementations, command-line tools
- **Commercial Use**: Allowed with full LGPLv3 compliance requirements
- **Source Code**: Available at [GitHub](https://github.com/RiV-chain/RiV-mesh)

#### Key GPLv3 Requirements:
- **Source Code Sharing**: Must provide Tensor source code when distributing
- **Application Code Sharing**: Must share source code of applications using Tensor
- **Build Instructions**: Must provide installation and build information
- **Modifications**: Any modifications to Tensor must remain open source

#### RiV-mesh™ LGPLv3 Requirements:
- **Source Code Sharing**: Must provide RiV-mesh™ source code when distributing
- **Application Code Sharing**: Must share source code of applications using RiV-mesh™
- **Build Instructions**: Must provide installation and build information
- **Modifications**: Any modifications to RiV-mesh™ must remain open source

For complete licensing details, see:
- [Core License](https://github.com/RiV-chain/RiV-mesh/blob/main/LICENSE) - LGPLv3

### 🔧 Troubleshooting

#### Common Tensor Issues

##### App Won't Start
If Tensor fails to launch:

1. **Check Android Version**: Ensure you're running Android 5.0+ (Lollipop)
2. **Restart Device**: Try restarting your Android device
3. **Clear App Data**: Go to Settings > Apps > Tensor > Storage > Clear Data
4. **Reinstall App**: Uninstall and reinstall Tensor from Google Play

##### VpnService Permission Issues
If you get permission errors:

1. **Grant VpnService Permission**: When prompted, allow Tensor to create VPN connections
2. **Check Device Admin**: Ensure Tensor has necessary device permissions
3. **Restart App**: Close and restart Tensor after granting permissions
4. **Check Other VPNs**: Disable other VPN apps that might conflict

##### Cannot Make Calls
If calls fail to connect:

1. **Check Mesh Network**: Ensure both devices are connected to RiV-mesh™ mesh
2. **QR Code Issues**: Rescan QR codes if contact exchange failed
3. **Network Connectivity**: Verify both devices have internet or local network access
4. **Contact Verification**: Ensure contact information was exchanged correctly

##### Call Quality Problems
If experiencing poor audio/video quality:

1. **Network Stability**: Check your internet connection or local network
2. **Device Performance**: Close other apps to free up resources
3. **Wi-Fi vs Mobile**: Try switching between Wi-Fi and mobile data
4. **Distance**: Ensure devices are within reasonable range for local mesh

##### Contact Exchange Issues
If QR code scanning fails:

1. **Camera Permissions**: Grant camera permission to Tensor
2. **QR Code Quality**: Ensure QR code is clear and well-lit
3. **Manual Entry**: Try manually entering contact information
4. **Network Sync**: Wait for mesh network to fully establish before exchanging contacts

#### Getting Help

- **Documentation**: [Tensor Documentation](docs/documentation.md)
- **Webpage**: [Tensor Community](https://cuplink.net)

* * *
