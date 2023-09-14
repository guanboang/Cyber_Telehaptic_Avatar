# System Installation and Usage Guide

## 🗃️ Resources

TactipEN.zip - This is the source code package for the UE5 system.
tactile_gym_finish.zip - This is the Tactile gym source code package with embedded communication plugins.

In addition, system installation requires dependencies on Quset Link. You will need to download the related installation package from the [Quest link](https://www.oculus.com/download_app/) official website and launch it after installation.

Unreal Engine 5 needs to be downloaded. You can download it from [Download Unreal Engine](https://www.unrealengine.com/en-US/download) and follow the prompts to install UE5.0.3.

The system requires Tactile Gym for simulation running, so you need to install Tactile Gym. A convenient method is to download and install Anaconda3 and create a Python3.8 environment. Run the following in the new environment:

```
python ***/***/tactile_gym_finish/setup.py install
```

Install as prompted. If there's a notification of missing packages, install the corresponding packages. If a VC++ toolset is not found, follow the prompt to visit the respective website and download and install the necessary package.

## 📒 Configuration

### Quest Link Connection
First, launch Oculus.
![image.png](https://guanboang.oss-cn-beijing.aliyuncs.com/img/20230914150821.png)

Select the Device tab and choose your device. Follow the instructions, depending on your situation, choose Air Link or connect via a USB3 cable. Configure the same settings in the headset.
![image.png](https://guanboang.oss-cn-beijing.aliyuncs.com/img/20230914151004.png)
After configuring, the headset will enter a white space. Note that after a successful connection, you can only interact using the controller.

### Starting Tactile Gym
After installing Tactile as mentioned above, you can launch Tactile Gym using the Anaconda virtual environment. For demonstration, start any routine from the tactile_gym_finish/examples folder. The method to start is:

```
python /tactile_gym_finish/example/demo_push_env.py
```

When you see the prompt: Server listening on 127.0.0.1:12345 (as shown in the picture)
![image.png](https://guanboang.oss-cn-beijing.aliyuncs.com/img/20230914152320.png)
It means Tactile Gym has started and is now listening on port 12345. If there's an error, check if port 12345 is occupied. The quickest way is to use the task manager to see the port usage.

### Launching Unreal Engine 5
Open Unreal Engine and select a recently opened project from the main screen:

![image.png](https://guanboang.oss-cn-beijing.aliyuncs.com/img/20230914152623.png)

Use the “Browse” tab to open the Tactip.uproject in the TactipEN folder. Once the Unreal Editor is fully opened, you will see the following interface:

![image.png](https://guanboang.oss-cn-beijing.aliyuncs.com/img/20230914152808.png)

This screen indicates that the system has been successfully launched. Click on the VR Preview at the top to enter the environment. In the environment, select the link in the menu to start using.

![image.png](https://guanboang.oss-cn-beijing.aliyuncs.com/img/20230914153445.png)

If you encounter a situation where the VR preview can't be selected as shown in the picture below, the quickest solution is to close Unreal Engine, check the Quest Link connection status, make sure it's connected, and then reopen Unreal Engine to use the VR preview.

![image.png](https://guanboang.oss-cn-beijing.aliyuncs.com/img/20230914152916.png)

