# คู่มือการติดตั้ง YOLOv12 Environment

### 📋 ข้อกำหนดระบบ (System Requirements)
- Python: 3.11 หรือขมากกว่า

### 🚀 การติดตั้งแบบ Step-by-Step

#### ติดตั้ง Ultralytics

```bash
# สร้าง venv
conda create -n yolov12 python=3.11
conda activate yolov12

python -m venv venv

# ติดตั้งจาก PyPI (แนะนำ)
pip install ultralytics

# หรือติดตั้งจาก GitHub (development version)
pip install git+https://github.com/ultralytics/ultralytics.git
```

#### Step 1: ตรวจสอบการติดตั้ง

```python
import torch
import ultralytics
from ultralytics import YOLO

print(f"PyTorch version: {torch.__version__}")
print(f"CUDA available: {torch.cuda.is_available()}")
print(f"Ultralytics version: {ultralytics.__version__}")

# ทดสอบโหลด model
model = YOLO('yolov12n.pt')
print("✅ YOLOv12 setup successful!")
```

### 🔧 การแก้ปัญหาที่พบบ่อย (Troubleshooting)

#### ปัญหา: Import errors
```bash
# อัพเดต pip
pip install --upgrade pip

# ติดตั้งใหม่
pip uninstall ultralytics
pip install ultralytics
# หรือเช็ค dependencies
```

###  Documents
หากมีปัญหา:
1. ตรวจสอบ [Ultralytics Issues](https://github.com/ultralytics/ultralytics/issues)
2. ดู [Documentation](https://docs.ultralytics.com/modes/predict/)
3. ถามใน community forums