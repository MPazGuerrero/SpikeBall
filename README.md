# **SpikeBall Event Dataset: Event-Based Ball Trajectories**

We present a neuromorphic dataset: SpikeBall+, based on  the Dynamic Vision Sensor, the dataset provides a collection of trajectory data elucidating the motion characteristics of a foosball ball. Leveraging the groundwork introduced in [1], this augmented database not only encompasses a wider range of ball trajectories but also implements enhancements to the criteria governing ball capture.

---

## **Dataset Overview**

The dataset consists of ball trajectory data categorized into three types of plays:
1. **Shots on Goal**:
   - Direct shots aimed at either the left or right goal.
2. **Short Plays**:
   - Simple plays with one or two rebounds of the ball.
3. **Complex Plays**:
   - Longer sequences with multiple rebounds and intricate ball movements.

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
├── DirectShots/
│   ├── SpikeBall+02.h5
│   ├── SpikeBall+09.h5
│   └── …
├── ShortPlays/
│   ├── SpikeBall+01.h5
│   └── …
├── ComplexPlays/
│   ├── SpikeBall+00.h5
│   └── …
├── examples/
│   └── trajectory_visualization.m
└── README.md
```
The dataset is provided in `.h5` format and organized into folders for each play type. Due to size constraints, some files are compressed in `.zip` format and need to be extracted before use

---

## **Usage**

### **Downloading the Dataset**
Clone this repository to access the dataset:

```bash
git clone https://github.com/MPazGuerrero/SpikeBallPlus.git
cd SpikeBallPlus/
```

---

### **References**

For more details, refer to the following article:

[1] Guerrero-Lebrero,M.P., Quintana,F. M., Guerrero,E. (2023). *SpikeBALL: Neuromorphic Dataset for Object Tracking.* Advances in Computational Intelligence - 17th International Work-Conference on Artificial Neural Networks, {IWANN} 2023, Ponta Delgada, Portugal, June 19-21, 2023, Proceedings, Part {II}, 14135, 641-652. Springer. [https://doi.org/10.1234/jnc.2023.12345](https://doi.org/10.1007/978-3-031-43078-7\_52)
