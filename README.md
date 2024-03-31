## <div align="center">RescueFly Propeller Inspection</div>

This repository offers the implementation of the propeller inspection that was performed at the [**Professorship of Computer Engineering**](https://www.tu-chemnitz.de/cs/ce) at the Chemnitz University of Technology based on the [**YOLOv5 framework**](https://ultralytics.com/yolov5) and within the scope of the [**RescueFly project**](https://rescuefly.org). The RescueFly project is a German state-funded project that has been funded by the [**German Federal Ministry for Digital and Transport**](https://bmdv.bund.de/EN/Home/home.html) for the duration from 01/01/2022 to 31/03/2024 under the number 45ILM1016D.

### Requirements

Clone this Git repository and install the YOLOv5 requirements that are listed in the `requirements.txt` file in a [**Python>=3.8.0**](https://www.python.org/) environment, including
[**PyTorch>=1.8**](https://pytorch.org/get-started/locally/).

<details open>
<summary>Install</summary>

```bash
$ git clone https://github.com/TU-Chemnitz-Prof-Technische-Informatik/RescueFly_TUC_UAV_Propeller_Inspection.git
$ cd RescueFly_TUC_UAV_Propeller_Inspection
$ pip install -r requirements.txt
```

</details>

### Inference

`detect.py` runs inference on a set of propeller images that should be stored in the folder `INPUTDIR` and that should be following the naming *Cam_n_image.jpg* where *n* should be a nubmer ranging from *1* to *6*, using the model that was trained for the purpose of detecting healthy and broken propellers within the RescueFly project, and saving the results to `OUTPUTDIR`.

```bash
python detect.py --source path/to/INPUTDIR --weights Propeller_Weights.pt --save-json --project path/to/OUTPUTDIR
```

### Citation

```shell
@inproceedings{ha2023vision,
  title={Vision-based Propeller Damage Inspection Using Machine Learning},
  author={Harras, Mohamed Salim and Saleh, Shadi and Battseren, Batbayar and Hardt, Wolfram},
  booktitle={Embedded Self Organizing Systems, Vol. 10 No. 7},
  pages={43--47},
  year={2023}
}
```

YOLOv5 is a family of object detection architectures and models and represents [**Ultralytics**](https://ultralytics.com) open-source research into future vision AI methods, incorporating lessons learned and best practices evolved over thousands of hours of research and development.

Our code is implemented using the YOLOv5 framework, so please remember to cite their work as well.
