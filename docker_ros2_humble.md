# 1) Crear directorio y Dockerfile
mkdir ~/ros2_humble_base
cd ~/ros2_humble_base
nano Dockerfile

# 2) Construir la imagen
sudo docker build -t ros2-humble-base .

# 3) Verificar que la imagen existe
sudo docker images | grep ros2-humble-base

# 4) Ejecutar un contenedor interactivo
sudo docker run -it --rm ros2-humble-base

# Dentro del contenedor (probar ROS 2)
ros2 --help
ros2 pkg list | head
printenv | grep ROS

# 5) Probar nodos de demo (Talker / Listener)
# Terminal 1 → Talker
sudo docker run -it --rm ros2-humble-base ros2 run demo_nodes_cpp talker

# Terminal 2 → Listener
sudo docker run -it --rm ros2-humble-base ros2 run demo_nodes_cpp listener

# 6) (Opcional) Montar un workspace persistente
mkdir -p ~/ros2_ws
sudo docker run -it --rm -v ~/ros2_ws:/root/ros2_ws ros2-humble-base

# Dentro del contenedor (para compilar)
cd ~/ros2_ws
mkdir -p src
apt update && apt install -y python3-colcon-common-extensions
colcon build
source install/setup.bash
