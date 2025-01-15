# 🚗 **SmartLicensePlateRecognition**

## **Overview**  
SmartLicensePlateRecognition is a cutting-edge machine learning project designed to identify and read vehicle license plates from images and video streams. Leveraging the power of **YOLOv5 (You Only Look Once)** for high-precision object detection and **OCR (Optical Character Recognition)** for text extraction, this system offers a seamless solution for various practical applications.  

The extracted license plate numbers are efficiently stored in a database for easy access and further analysis.  

### **Applications**  
- Intelligent traffic management  
- Automated parking systems  
- Electronic toll collection  
- Surveillance and law enforcement  

---

## 🛠️ **Features**  
- **High-Performance Detection:** Robust license plate localization under diverse conditions (lighting, weather, etc.).  
- **OCR Integration:** Extracts alphanumeric details from detected plates.  
- **Real-Time Compatibility:** Processes both live video streams and static images.  
- **Custom Dataset Training:** Easily train the detection model for region-specific license plate styles.  
- **Database Support:** Automated storage of plate numbers for enhanced record-keeping.  
- **Platform Independence:** Deployable on Windows, Linux, or cloud infrastructure.  

---

## 🔧 **Installation**  

### **Dependencies**  
Install the following libraries and frameworks to get started:  
- TensorFlow  
- torch  
- torchvision  
- numpy  
- opencv-python  
- matplotlib  
- pytesseract  
- Pillow  

Use the following command to install all dependencies at once:  
```bash  
pip install -r requirements.txt  
```
### **1. Clone the Repository**  
```bash  
git clone https://github.com/YOUR_USERNAME/SmartLicensePlateRecognition.git  
cd SmartLicensePlateRecognition  
```
### **2. Set Up YOLOv5**  
Download and configure YOLOv5:  
```bash  
git clone https://github.com/ultralytics/yolov5.git  
cd yolov5  
pip install -U -r requirements.txt  
```
### **3. Dataset Preparation**  
Organize your dataset as shown below:  
```plaintext  
dataset/  
├── annotations/  
│   ├── test/  
│   ├── train/  
│   └── validation/  
├── images/  
│   ├── test/  
│   ├── train/  
│   └── validation/  
```
### **4. Annotation Conversion**  
Convert XML annotation files into YOLO-compatible `.txt` format. A script named `convert_xml_to_txt.py` is included for this purpose. Update the paths in the script to match your local dataset structure before running it:  
```bash  
python convert_xml_to_txt.py  
```
### **5. Model Training**  
Train the YOLOv5 model on your custom dataset using the following command:  
```bash  
python train.py --img 640 --batch 8 --epochs 50 --data data.yaml --weights yolov5s.pt --device 0  
```
--img: Input image size (default 640).
--batch: Number of images per batch.
--epochs: Total training epochs.
--data: Path to your dataset configuration file.
--weights: Pretrained model weights.
--device: GPU/CPU for training (0 for GPU, cpu for CPU)

## 🧪 **Testing & Evaluation**  
(Coming Soon)  
The testing pipeline will evaluate the model's performance on unseen images and videos to measure metrics like accuracy, precision, and recall.
