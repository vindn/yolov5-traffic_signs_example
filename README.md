# yolov5-traffic_signs_example

Exemplo Simples de Reconhecimento de 4 Tipos de Imagens de Sinais Trâsito utilizando o YOLOv5

- 4 Classes:
-- Semaphore
-- Stop Sign
-- Speed Limit Sign
-- Cross Walk

0. Pré requisitos:

- Instalação do CUDA;
- Instalação com OpenCV com CUDA;
- Instalação do Pytorch;

1. O labels das imagens foram criados utilizando o labelImg e salvos no formato XML;
2. Foi utilizando o site Roboflow para converter as imagens e labels para o formato do YOLOV5 e separar o dataset em train, val e test;
3. Para treinar o modelo utilizar o script do YOLOv5:
 
#python3 yolov5/train.py --img 412 --batch 16 --epochs 10 --data data.yaml --cache
 
4. Para utilizar o modelo treinado e prever as placas na webcam utilizar (altere o caminho do peso gerado pelo treinamento):

#python3 yolov5/detect.py  --source 0 --weight runs/train/exp11/weights/best.pt --img 416 --conf 0.25

5. Arquivo do Jupyter Notebook disponibilizado para manipulação do modelo treinado.
