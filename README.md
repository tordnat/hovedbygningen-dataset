# Hovedbygningen Dataset

Stereo SfM dataset of the main building of the Norwegian University of Science and Technology (NTNU) in Trondheim, captured with an open-source handheld stereo rig. The dataset was created for the master's thesis *Accelerating COLMAP: An Open-Source Software Contribution* (NTNU, 2026), where it serves as a real-world case study for Caspar BA, the GPU bundle adjustment backend released in COLMAP 4.1.0.

<iframe
  src="https://natlandsmyr.com/hovedbygningen-dataset/ply_point_cloud_viewer.html"
  width="100%"
  height="500px"
  style="border:none; border-radius:8px;">
</iframe>

*Interactive preview: sparse COLMAP reconstruction of the Hovedbygningen sequence. Click to fly (WASD + mouse, scroll to change speed, ESC to release).*

## The sequences

The dataset contains three sequences, each captured in a single handheld traversal. Because each stereo frame overlaps mainly with its temporal neighbours, the sequences have the low covisibility typical of structured survey-style captures. Unlike most curated benchmarks, the sequences were captured with a fully documented rig that others can rebuild, and every sequence includes synchronized IMU data.

| Sequence | Images | Stereo pairs | Scene | Trajectory |
|---|---|---|---|---|
| **Hovedbygningen** | 300 | 150 | NTNU main building exterior | Single pass, no loop closure |
| **Hovedbygningen Loop** | 658 | 329 | NTNU main building exterior | Full loop around the building |
| **Ohma** | 252 | 126 | The locomotive *Ohma Electra* | Orbit around the object |

All sequences provide:

- Rectified stereo image pairs at 2208 × 1242 pixels
- Factory-calibrated camera intrinsics and stereo extrinsics
- IMU measurements, timestamped against the same clock as the images

The calibrated stereo baseline fixes the scale of the reconstruction, so the sequences support metric reconstruction without external ground control.

## The capture rig

The sequences were recorded with a custom two-handed capture rig built around a Stereolabs ZED 2i stereo camera (2.1 mm focal length, polarizing filter) and an NVIDIA Jetson Nano. The rig is remote-controlled from a smartphone over WiFi, weighs roughly 1 kg, and is designed to be reproducible with a 3D printer and off-the-shelf parts.

Design files, bill of materials, and capture software are open source: [tordnat/stereo_capture_rig](https://github.com/tordnat/stereo_capture_rig).

## Download

*[Download link](https://drive.google.com/file/d/1h4xDytiXU9uOH0J_rufSAdYXJ_FDYlys/view?usp=sharing)*

## Citation

If you use this dataset, please cite:

> Tord Natlandsmyr. *Accelerating COLMAP: An Open-Source Software Contribution.* Master's thesis, Norwegian University of Science and Technology, 2026.

## License

Released under the [MIT License](LICENSE).
