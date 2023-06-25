This is Yolo-client Ochestration using kubernetes.
The images used were containerized using docker and pushed to docker hub.
1. rwambui/yolo-client:1.0.0
2. rwambui/yolo-backend:1.0.0

pvc file is created to provision storage volumes.
The pvc is then used to mount the storage volume to Pods.
PersistentVolumeClaim was used to ensure application's data persists even if the Pod is restarted or rescheduled.