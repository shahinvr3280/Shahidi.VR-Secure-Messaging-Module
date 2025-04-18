# Shahidi.VR Secure Voice Messaging

**Version:** 0.1.0 (MVP)

This component implements a secure, end-to-end encrypted voice channel using WebRTC, which by default uses DTLS for key exchange and SRTP with AES-GCM-256 for media encryption.

## Features
- 1:1 voice call with microphone capture and playback
- ICE-based NAT traversal
- DTLS handshake for SRTP AES-256-GCM encryption
- PeerConnection-based signaling (requires external signaling server)

## Prerequisites
- **Android**: Android Studio 2022+, NDK r23+, Kotlin 1.7
- **iOS**: Xcode 14+, Swift 5.7, CocoaPods
- External signaling server (WebSocket or HTTP REST) to exchange SDP and ICE.

## Integration

### Android
1. Copy the `android/` folder into your Unity `Plugins/Android/` or open as a standalone Android module.  
2. Ensure your `build.gradle` contains:
   ```groovy
   implementation 'org.webrtc:google-webrtc:1.0.32006'
