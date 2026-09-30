# Wi-Fi Generation Comparison Tool

Describe what you need in plain English. The tool works out the bandwidth required and checks every Wi-Fi generation against it.

Max speed is the theoretical link rate from the standard. Real-world throughput is a typical usable figure for one router.

### How the estimate is made

- **Reading your sentence:** the tool looks for the number of devices and for activity keywords such as gaming, streaming, calls, downloads.
- **Speed per device:** each activity has a typical bandwidth. With several activities, the heaviest counts fully and the others add 30%.
- **Total required:** `devices × speed per device × 1.25`. The 25% is headroom for overhead and interference.
- **Usable capacity:** `real throughput ÷ (1 + k × (devices − 1))`. The factor k models contention; newer generations have a smaller k because of MU-MIMO and OFDMA.
- **Verdict:** usable speed per device compared with the requirement, plus a latency check for gaming and VR.

This is an educational estimation model. All devices are assumed to be active at the same time, which is the worst case. Actual results depend on router hardware, walls, distance and channel width.