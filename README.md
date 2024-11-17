<p align="center">
<img src="./assets/images/dtlogo.png" alt="Duckietown Logo" width="50%">
</p>

# **Learning Experience (LX): <LX_TITLE_HERE>**

# About these activities

<DESCRIPTION_HERE>

In this learning experience, you will ... **TODO: Describe the LX activities and outcome here**

This learning experience is provided by the Duckietown team and can be run on Duckiebots. Visit us at the 
[Duckietown Website](https://www.duckietown.com) for more learning materials, documentation, and demos.

For guided setup instructions, lecture content, and more related to this LX, see **TODO: Add course link here**.

## Grading challenge

**TODO: Add optional challenge link or remove the `Grading challenge` section**

# Instructions

**TODO: Update Step 1. to match your learner setup**

**NOTE:** All commands below are intended to be executed from the root directory of this exercise (i.e., the directory containing this README).


## 1. Make sure your exercise is up-to-date

Update your exercise definition and instructions,

    git pull upstream <your upstream branch>

**NOTE:** Example instructions to fork a repository and configure to pull from upstream can be found in the [duckietown-lx repository README](https://github.com/duckietown/duckietown-lx/blob/mooc2022/README.md).


## 2. Make sure your system is up-to-date

- 💻 Always make sure your Duckietown Shell is updated to the latest version. See [installation instructions](https://github.com/duckietown/duckietown-shell)

- 💻 Update the shell commands: `dts update`

- 💻 Update your laptop/desktop: `dts desktop update`

- 🚙 Update your Duckiebot: `dts duckiebot update ROBOTNAME` (where `ROBOTNAME` is the name of your Duckiebot chosen during the initialization procedure.)


## 3. Work on the exercise

### Launch the code editor

Open the code editor by running the following command,

```
dts code editor
```

Wait for a URL to appear on the terminal, then click on it or copy-paste it in the address bar
of your browser to access the code editor. The first thing you will see in the code editor is
this same document, you can continue there.


### Walkthrough of notebooks

**NOTE**: You should be reading this from inside the code editor in your browser.

Inside the code editor, use the navigator sidebar on the left-hand side to navigate to the
`notebooks` directory and open the first notebook.

Follow the instructions on the notebook and work through the notebooks in sequence.


### Building your code

You can build your code with 

```
dts code build -R ROBOT_NAME
```

This will build a docker image with your code compiled inside - you should your ROS node get built during the process. 


### Testing with Duckiematrix

In order to test your code in the Duckiematrix you will need a virtual robot. You can create one with the command:

```
dts duckiebot virtual create [VBOT]
```

where `[VBOT]` can be anything you like (but remember it for later).

Then you can start your virtual robot with the command:

```
dts duckiebot virtual start [VBOT]
```

You should see it with a status `Booting` and finally `Ready` if you look at `dts fleet discover`: 

```
     | Hardware |   Type    | Model |  Status  | Hostname 
---  | -------- | --------- | ----- | -------- | ---------
[VBOT] |  virtual | duckiebot | DB21J |  Ready   | [VBOT].local
```

Now that your virtual robot is ready you can start the Duckiematrix. From this exercise directory do:

```
dts code start_matrix
```

You should see the Unity-based Duckiematrix simulator start up. 


### 💻 Testing 


To test your code in the duckiematrix you can do:

```
dts code workbench -m -R [VIRTUAL_ROBOT_NAME]
```

and to test your code on your real Duckiebot you can do:

```
dts code workbench -R [ROBOT_NAME]
```


In another terminal, you can launch the `noVNC` viewer for this exercise which can be useful to send commands to the robot and view the odometry that you calculating in the RViZ window. 

```
dts code vnc -R [ROBOT_NAME]
```

where `[ROBOT_NAME]` could be the real or the virtual robot (use whichever you ran the `dts code workbench` and `dts code build` command with).


Now you can proceed to the [first notebook](ADD_LINK_TO_NOTEBOOK).
