# papers_with_code
Documentación inicial. Este archivo será completado más adelante con actividades, evidencias, y análisis.
[Uploading repro_yolov8_coco128.ipynb…]()
# reproducir_experimento.py (fragmentos)
from ultralytics import YOLO
import pandas as pd
import matplotlib.pyplot as plt
import json
import os


# 1. Cargar modelo preentrenado (yolov8n)
model = YOLO('yolov8n.pt')


# 2. Entrenar (config desde Python)
results = model.train(data='coco128.yaml', epochs=3, imgsz=640, batch=16)


# 3. Guardar el objeto results y métricas
# Ultralytics guarda resultados en 'runs/detect/train'
run_dir = None
for root, dirs, files in os.walk('runs'):
if 'train' in root and 'weights' in root:
run_dir = root
break


# Alternativamente: leer el archivo results.csv generado por ultralytics
res_csv = os.path.join('runs', 'train', 'results.csv')
if os.path.exists(res_csv):
df = pd.read_csv(res_csv)
df.to_excel('resultados_entrenamiento.xlsx', index=False)
else:
print('No se encontró results.csv en la ruta esperada. Revisa runs/train/')


# 4. Ejemplo para graficar loss, precision y recall si están en el dataframe
if 'box_loss' in df.columns:
plt.figure()
plt.plot(df['epoch'], df['box_loss'], marker='o')
plt.title('Box Loss por época')
plt.xlabel('Epoch')
plt.ylabel('Box Loss')
plt.grid(True)
plt.savefig('loss_box.png')


if 'mAP_0.5' in df.columns:
plt.figure()
plt.plot(df['epoch'], df['mAP_0.5'], marker='o')
plt.title('mAP@0.5 por época')
plt.xlabel('Epoch')
plt.ylabel('mAP@0.5')
plt.grid(True)
plt.savefig('map50.png')


print('Ejecución finalizada. Revisa archivos generados.')
