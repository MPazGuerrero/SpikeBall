# **SpikeBall Event Dataset: Event-Based Ball Trajectories**

We present a neuromorphic dataset: SpikeBall, based on  the Dynamic Vision Sensor, the dataset provides a collection of trajectory data elucidating the motion characteristics of a foosball ball. 


## **Dataset Overview**

The dataset consists of two folders:
1. **Trajectories**:
   - Ball trajectories with annotated ball-center positions, including direct hits, simple trajectories, and trajectories with up to two bounces.
2. **Splits**:
   - It includes predefined training, validation, and test splits in CSV and TXT formats.


---

## **Data Format**

The data is structured as a collection of events, where each event represents a significant change in the ball's state. The key attributes for each event include:

| Field          | Description                                     |
|-----------------|-------------------------------------------------|
| `timestamp`    | Time of the event in microseconds               |
| `x`            | X-coordinate of the ball                       |
| `y`            | Y-coordinate of the ball                       |
| `polarity`     | Indicates the direction of intensity change: 1 for an increase (brightening) and 0 for a decrease (darkening) |
| `x_center`     | The x-coordinate of the ball’s center |
| `y_center`     | The y-coordinate of the ball’s center |

The dataset is provided in `.h5` format and organized into folders for each play type. Due to size constraints, some files are compressed in `.zip` format and need to be extracted before use

---

## **Folder Structure**
```plaintext
SpikeBallPlus/
│
├── Trajectories/
│   ├── SpikeBall02.h5
│   ├── SpikeBall09.h5
│   └── …
├── Splits/
│   ├── train.txt
│   ├── train.csv
│   └── …
└── README.md
```
The dataset is provided in `.h5` format and organized into folders for each play type. Due to size constraints, some files are compressed in `.zip` format and need to be extracted before use

---

## **Usage**

### **Downloading the Dataset**
Clone this repository to access the dataset:

```bash
git clone https://github.com/MPazGuerrero/SpikeBall.git
cd SpikeBall/
```

---

### **References**

For more details, refer to the following article:

[1] Guerrero-Lebrero,M.P., Quintana,F. M., Guerrero,E. (2023). *SpikeBALL: Neuromorphic Dataset for Object Tracking.* Advances in Computational Intelligence - 17th International Work-Conference on Artificial Neural Networks, {IWANN} 2023, Ponta Delgada, Portugal, June 19-21, 2023, Proceedings, Part {II}, 14135, 641-652. Springer. ([https://doi.org/10.1007/978-3-031-43078-7\_52](https://dl.acm.org/doi/10.1007/978-3-031-43078-7_52))
