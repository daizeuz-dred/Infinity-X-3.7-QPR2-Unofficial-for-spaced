# Infinity-X-3.7-QPR2-Unofficial-for-spaced

🚀 Performance & System
Power Management: Reworked PowerHint implementation with a shift to policy-based power nodes for better efficiency.
CPU Tuning: Optimized schedutil up/down rate limits for snappier frequency scaling.
Memory Management: * Increased zRAM allocation to 70% of total RAM.
Adjusted swappiness to 70 and disabled zRAM writeback to reduce disk I/O.
Updated Low Memory Killer (LMK) properties for better multitasking.
Graphics & Rendering: * Allocated 4 buffers to SurfaceFlinger for smoother frame delivery.
Raised SurfaceFlinger region sampling frequency.
Imported Motorola phase offsets; dropped legacy phase durations and multi-threshold tuning.
Cleanup: Removed MediaTek gauge, legacy power properties, mmstat tracing, and the compat namespace.
Toolchain: Stopped pinning kernel Clang version and overrode kernel BPF version for improved build flexibility.

🎮 Display & UI
High Refresh Rate: Enabled 120Hz support for gaming.
Animation Refinement: * Simplified activity open/close transitions.
Switched to linear interpolators for a more consistent feel.
Dynamic animation scaling based on screen percentage.
Visual Enhancements: * Reduced blur radius in overlays and added support for rounded corners.
Adjusted status bar padding for better alignment.
Refresh Rate Logic: Reverted "Smooth Display" in favor of explicit min/peak refresh rate toggles.

🔋 Memory & Runtime
ART/Dalvik: Reverted dynamic heap overrides and grouped property initializations to improve stability.
Legacy Cleanup: Removed Android 11 libinit adaptations and cleaned up stale includes.
Core System: Migrated system/core/base changes for better upstream compatibility.

📡 Connectivity & Audio
NFC: Modernized stack by switching to AIDL NXP NFC HAL and refining the configuration.
Audio: * Optimized mute duration handling.
Stripped unused codecs and MTK encoder performance hints.
Disabled Audio HAL PCM dumping and dropped Dolby Atmos for a leaner audio path.

🧩 Sensors & HAL
Sensor Stack: Added Dynamic Sensors HAL support.
Compatibility: Linked MTK sensor multihal with libbase shim and patched blobs to utilize libtinyxml2-v34.

🔐 Security & Filesystem
Security: Disabled Factory Reset Protection (FRP) for development flexibility.
Filesystem: Implemented metadata_csum for the /metadata partition.
Cleanup: Purged duplicate blobs and redundant vendor framework matrices.

🧱 Build System & Fixes
Blueprint Migration: Converted rootdir to Blueprint for modern build standards.

Maintenance: Renamed Lineage overlays and removed unused/duplicate configurations.

Bug Fix: Resolved permission issues for opluserserve1.
