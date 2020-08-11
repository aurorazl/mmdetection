训练启动：  
    python tools/train.py configs/pascal_voc/faster_rcnn_r50_fpn_1x_voc0712.py --gpus 1 --work-dir work-dirs

测试：
    python tools/test.py configs/faster_rcnn/faster_rcnn_r50_fpn_1x_coco.py work-dirs/epoch_4.pth --eval bbox
    python tools/test.py configs/faster_rcnn/faster_rcnn_r50_fpn_1x_coco.py work-dirs/epoch_4.pth --show
    python tools/test.py configs/faster_rcnn/faster_rcnn_r50_fpn_1x_coco.py work-dirs/epoch_4.pth --show-dir result --show-score-thr 0.1
    
测试单个图片：
    python demo/image_demo.py /data/work/tony/storage/1596533371098/JPEGImages/20190902_1001_009.jpg configs/faster_rcnn/faster_rcnn_r50_fpn_1x_coco.py work-dirs/epoch_4.pth --device cpu