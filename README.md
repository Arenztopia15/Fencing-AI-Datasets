# Fencing-AI-Datasets

A list of public datasets and dataset-like resources for AI, machine learning, computer vision, pose estimation, action recognition, and referee-assistance work for the Olympic sport of fencing. This list is not exhaustive. If you find a new dataset, a working download link, or updated release status for an unverified item, please update the repository.

Status tags:

- **Dataset**: public data download or dataset page found.
- **Benchmark / paper release**: paper describes a public benchmark or release, but a direct standalone data URL may need verification.
- **Code / pipeline**: public code for collecting, processing, or modeling fencing data, but not a formal benchmark dataset.
- **Needs verification**: public lead found or reported, but dataset availability could not be confirmed from indexed sources.

* **Public datasets**
  1. [Fencing Footwork Dataset (FFD)](https://home.agh.edu.pl/~fmal/ffd/): **Dataset.** Contains 6 fencing footwork actions: step forward, step backward, rapid lunge, incremental-speed lunge, lunge with waiting, and jumping-sliding lunge. Includes samples from 10 fencers, recorded with Kinect and x-IMU. Data includes Kinect skeleton files, Kinect depth videos, accelerometer, gyroscope, magnetometer, and IMU rotation data; RGB is not included. The official page provides a Google Drive download; zipped size is about 1 GB and unzipped size is over 30 GB. [[FenceNet paper]](https://openaccess.thecvf.com/content/CVPR2022W/CVSports/papers/Zhu_FenceNet_Fine-Grained_Footwork_Recognition_in_Fencing_CVPRW_2022_paper.pdf) [[arXiv]](https://arxiv.org/abs/2204.09434)
  2. [Sport : Fencing Matches AI](https://www.kaggle.com/datasets/alexpgd/sport-fencing-matches-ai): **Dataset.** Kaggle dataset for AI work on fencing match/referee decisions. The FACTS paper cites it as a prior fencing-AI dataset/resource using pose estimation and CNN-LSTM-style modeling. Kaggle pages are JavaScript-rendered, so file counts, license, and current download status should be rechecked directly on Kaggle before reuse. [[Referenced in FACTS]](https://arxiv.org/abs/2412.16454)

* **Benchmarks / paper releases**
  1. [FACTS - Fine-Grained Action Classification for Tactical Sports](https://arxiv.org/abs/2412.16454): **Benchmark / paper release.** Introduces a fine-grained tactical-sports action-recognition benchmark with fencing and boxing. The fencing portion is described as raw-video based, sourced from Quarte Riposte competition footage, and reduced from 13,459 annotated clips to 6,400 final clips after filtering/augmentation. It uses 8 fencing labels: attack left/right, riposte left/right, counter-attack left/right, and remise left/right. The paper says the dataset/preprocessed data are public, but a separate dataset URL was not found in the arXiv metadata or indexed search results.
  2. [FERA - Foil Fencing Referee Assistant](https://arxiv.org/abs/2509.18527): **Benchmark / paper release.** Describes a foil-fencing referee-assistance benchmark built from professional broadcast bouts. The paper reports 493 underlying clip IDs, 598 matched labeled pose-view files, 1,800 cleaned labeled segments, 11 move labels, and 5 blade-position labels. It states that only anonymized pose features, labels, and code are released. A direct download or GitHub URL was not found in the arXiv metadata or indexed search results, so release status should be verified before treating it as a downloadable dataset.

* **Code and dataset-building pipelines**
  1. [sholtodouglas/fencing-AI](https://github.com/sholtodouglas/fencing-AI): **Code / pipeline.** Public repository for deep-learning-based fencing refereeing. The README describes downloading fencing match videos, cutting short clips before scoreboard light events, auto-labeling some referee-decision clips from scoreboard changes, downsampling, horizontal flipping, optical-flow overlay generation, and model training. The repo reports roughly 5,500 clips, or about 11,000 after horizontal flipping, but does not publish a formal dataset release.
  2. [GalDude33/fencing-AI](https://github.com/GalDude33/fencing-AI): **Code / pipeline.** Public repository extending fencing-referee modeling with pose estimation, optical flow, and C3D-style modeling. The README describes building clips from the 50 frames before scoreboard light events and deriving labels from score differences. Useful as a data-generation/modeling reference, but not a formal benchmark dataset release.
  3. **RT-Fencing**: **Needs verification.** Public code/repo lead for real-time fencing analysis. Dataset status and canonical URL could not be verified from indexed web search results. Add the repository URL, license, and whether data are downloadable once confirmed.

* **Related research leads**
  1. [VirtualFencer - Generating Fencing Bouts based on Strategies Extracted from In-the-Wild Videos](https://arxiv.org/abs/2507.00261): **Related research.** System for extracting 3D fencing motion and strategy from in-the-wild video and generating fencing behavior. Useful as a lead for motion/strategy modeling, but no public dataset release was found in indexed search results.
  2. [FenceNet - Fine-Grained Footwork Recognition in Fencing](https://arxiv.org/abs/2204.09434): **Related paper.** Not a separate dataset, but an important model paper using FFD. Reports FFD as 652 videos from 10 fencers and 6 footwork classes, with 3D skeleton, depth, and IMU signals.

## Notes for contributors

- Prefer resources with a direct public data URL, license, and citation.
- Keep code-only repositories separate from benchmark datasets.
- Mark resources as **Needs verification** when a paper or repo claims a release but no direct public download is visible.
- For Kaggle or Google Drive resources, verify the license and access requirements before training or redistributing derived data.
