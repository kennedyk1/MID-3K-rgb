# MID-3K — RGB modality

[Main dataset repository](https://github.com/kennedyk1/MID-3K) · [Dataset website](https://kennedyk1.github.io/MID-3K/) · [Metadata](https://github.com/kennedyk1/MID-3K/blob/main/metainfo.csv)

This repository contains the RGB images and person annotations for the MID-3K Multimodal ISR Dataset, collected with a Clearpath Jackal at DEEC and DEI, University of Coimbra.

## Repository contents

| Path | Format | Count | Description |
| --- | --- | ---: | --- |
| `images/` | PNG, 640 × 512 | 3,083 | RGB dataset images |
| `labels/` | TXT, YOLO `xywhn` | 3,083 | Person annotations |

Dataset size: approximately **1.3 GB**. The repository contains **10,824** person annotations.

## Sensor

| Field | Value |
| --- | --- |
| Camera | Ximea MQ013CG-E2 |
| Sensor type | Colour camera |
| Native sensor resolution | 1280 × 1024, 1.3 MP |
| Dataset image resolution | 640 × 512 |

Each label line uses normalized YOLO format:

```text
class x_center y_center width height
```

## Calibration and association

The COLOR–LiDAR and COLOR–THERMAL matrices are maintained in the main dataset repository:

- [COLOR camera from LiDAR](https://github.com/kennedyk1/MID-3K/blob/main/calibration/color_lidar/calibration.yaml)
- [THERMAL camera from COLOR camera](https://github.com/kennedyk1/MID-3K/blob/main/calibration/color_thermal/calibration.yaml)

Use [`metainfo.csv`](https://github.com/kennedyk1/MID-3K/blob/main/metainfo.csv) for scene metadata and reproducible data splits. The raw LiDAR scans are available in [MID-3K-pcd](https://github.com/kennedyk1/MID-3K-pcd).

## Related repositories

| Data | Repository |
| --- | --- |
| Thermal images | [MID-3K-thermal](https://github.com/kennedyk1/MID-3K-thermal) |
| Depth images | [MID-3K-depth](https://github.com/kennedyk1/MID-3K-depth) |
| Intensity images | [MID-3K-intensity](https://github.com/kennedyk1/MID-3K-intensity) |
| Raw LiDAR point clouds | [MID-3K-pcd](https://github.com/kennedyk1/MID-3K-pcd) |
