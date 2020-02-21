## HOWTO 

    docker run -it -v $(pwd):/data --entrypoint ffmpeg linuxserver/ffmpeg -r 1 -t 3600 -i /data/ch01_20200218174001.avi -f image2 /data/input/image-%04d.jpg

    // in detectron path
    python demo/demo.py \
    --config-file configs/COCO-Detection/faster_rcnn_R_50_FPN_3x.yaml \
    --input ~/projects/omega/perception/01_detect_car/input/* \
    --output ~/projects/omega/perception/01_detect_car/output \
    --opts MODEL.WEIGHTS detectron2://COCO-Detection/faster_rcnn_R_50_FPN_3x/137849458/model_final_280758.pkl

    python demo/demo.py \
    --config-file configs/PascalVOC-Detection/faster_rcnn_R_50_FPN.yaml \
    --input ~/projects/omega/perception/01_detect_car/input/* \
    --output ~/projects/omega/perception/01_detect_car/output2 \
    --opts MODEL.WEIGHTS detectron2://Cityscapes/mask_rcnn_R_50_FPN/142423278/model_final_af9cf5.pkl

    docker run -it -v $(pwd):/data --entrypoint ffmpeg linuxserver/ffmpeg -f image2 -i /data/output/image-%04d.jpg /data/output.mp4

## TODO
- demo.py에 직접 video를 넣어보자