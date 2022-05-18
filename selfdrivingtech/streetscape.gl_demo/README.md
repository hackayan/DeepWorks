# My work on streetscape.gl project #


## Project: Visualize Xviz protocol transformed data with streetscape.gl ##

### Step 1: Get Xviz protocol supported data 
- Downalod Xviz transformed data for KITTI dataset
  - $ wget https://raw.githubusercontent.com/uber/xviz-data/master/kitti/2011_09_26_drive_0005_sync/0-frame.json
  - $ wget https://raw.githubusercontent.com/uber/xviz-data/master/kitti/2011_09_26_drive_0005_sync/{1..155}-frame.glb
  - Note: You should have 1 0-frame.json and 155 {1..155}-frame.glb files, total 156 files
- Download Xviz transformed data for NuScenes V0.1 dataset
  - $ wget https://raw.githubusercontent.com/uber/xviz-data/master/nutonomy/scene-0006/0-frame.json
  - $ wget https://raw.githubusercontent.com/uber/xviz-data/master/nutonomy/scene-0006/{1..390}-frame.glb
  - Note: You should have 1 0-frame.json and 390 {1..390}-frame.glb files, total 391 files

### Step 2: Get (Familiarize yourself) with the streetscape.gl code and example
- Streetscape Source: https://github.com/aurora-opensource/streetscape.gl
- Get get-started sample from the steetscape.gl project
  - https://github.com/aurora-opensource/streetscape.gl/tree/master/examples/get-started
- Review the above code
- Note this code is designed to read the KITTI dataset directly from the web
- You don't need to download any dataset locally on your machine to make this sample works
- How to run
  - yarn or npm install
  - {npm | yarn} start
    - Visit http://localhost:8080

### Step 3: Update existing streetscape.gl example to React 17 and Chakra UI with my code
- Please download the streetscape-demo folder located here
- Add your both kitti and NuScenes data you have downloaded in the step 1
  - Create a folder name 'kitti/2011_09_26' in the project root
    - Copy all the files (0-frame.json and 0-frame.glb to 153-frame.glb) into the 2011_09_26 sub-folder
  - Create folder/subfolder name(s) 'nuscenes/v0.1' in the project root
    - Copy all the files (0-frame.json and 0-frame.glb to 153-frame.glb) into the v0.1 sub-folder
- Your Prject Tree should look like as below
  - index.html
  - kitti
    - 2011_09_26 (This folder should have total 156 files)
  - nuscenes
    - v0.1 (This folder should have total 391 files)
  - node_modules
  - src
  - package.json
- How to Run the example:
  - npm install
  - npm start
    - Visit http://localhost:8080