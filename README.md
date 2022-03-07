# Joint Camera Intrinsic and LiDAR-Camera Extrinsic Calibration. 
This is a project for LiDAR to camera joint calibration. For more calibration codes, please refer to the link <a href="https://github.com/PJLab-ADG/SensorsCalibration" title="SensorsCalibration">SensorsCalibration</a>


## Prerequisites

- Cmake
- Opencv 2.4.13
- PCL 1.9

## Compile
Compile in their respective folders

```shell
# mkdir build
mkdir -p build && cd build
# build
cmake .. && make
```


## Usage

1. Two Input files: 

   `./lidar2camera camera_dir csv_file`

- **camera_dir**: Collected camera calibration board data
- **csv_file**: The circles center points corresponding to the images

**Note:** To extract the circles center form PCD files, please refer to [README.md](tool/README.md).

2. Run the test sample:

   The executable file is under the bin folder.

   ```
   cd ~./lidar2camera/joint_calib
   ./bin/lidar2camera data/intrinsic/ data/circle.csv
   ```

3. Calibration result:

   <img src="./result/refine0.png" width="100%" height="100%" alt="Calibration result" div align=center />
   <img src="./result/refine1.png" width="100%" height="100%" alt="Calibration result" div align=center />
   <img src="./result/refine4.png" width="100%" height="100%" alt="Calibration result" div align=center />
   <img src="./result/refine8.png" width="100%" height="100%" alt="Calibration result" div align=center />

## Citation
This code is based on the research below:
```
@misc{2202.13708,
Author = {Guohang Yan and Feiyu He and Chunlei Shi and Xinyu Cai and Yikang Li},
Title = {Joint Camera Intrinsic and LiDAR-Camera Extrinsic Calibration},
Year = {2022},
Eprint = {arXiv:2202.13708},
}
   
```
