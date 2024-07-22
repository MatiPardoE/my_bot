## Para simulacion con Nav2

1. hacer source install/setup.bash desde my_bot
2. ros2 launch my_bot launch_sim.launch.py world:=./src/my_bot/worlds/TubeWorldV4.world  lanza la simulacion
3. en otra ventana hacer source y abrir el slam con el mapa cargado:
    - ros2 launch my_bot online_async_launch.py params_file:=./src/my_bot/config/mapper_params_online_async.yaml use_sim_time:=true
4. Nav2
    - ros2 launch nav2_bringup navigation_launch.py use_sim_time:=true
5. Abrir Rviz y configurar