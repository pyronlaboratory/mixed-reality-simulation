# 700119_002_CWRK
Mixed Reality Simulation of Airway Insertion Medical Training


**Context**

Anaesthetising patients for surgery can be an unpredictable challenge, with risks for the patient. This is especially true in patients who have disease affecting their airway, such as Covid-19, cancer of the throat or other areas of the head and neck. It often involves a technique called fibreoptic intubation (where a flexible videoscope if navigated through the airways to pass a breathing tube). Developing a training tool that allows anaesthetists to plan and practice the management of these difficult situations, in a 3D mixed reality environment, may help deliver safer care.

Airway fibreoptic intubation and the manipulation of the controller are illustrated in this [video demonstration](https://www.youtube.com/watch?v=hrYkgXLNNsA).

A hardware simulator with usual 3D graphics can be found [here](https://www.orsim.com). 

Similar projects with VR/AR simulation can be found in the references ([Casso 2019](https://journals.lww.com/anesthesia-analgesia/fulltext/2019/11000/development_and_initial_evaluation_of_a_novel,.14.aspx), [Agasthya 2020](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7802606/)).

 

**Methods**

The project is to design and implement a HoloLens 2 AR App with potential application to medical training of airway fibreoptic intubation. The main tools and development environment for the completion of the coursework will be Unity, Microsoft Visual Studio and HoloLens 2 device. 3D models of the airway will be provided. A simple model of controller and fibreoptic cable should be designed using Unity rigid and soft-body. Alternatively, you can search and download the assets of 3D airway model and controller/cable models from somewhere else. 

The 3D airway model is provided in fbx format.

Firstly, the project will use core mixed reality features including Mixed Reality Toolkit (MRTK), Positioning, Interacting, Eye tracking and Voice commands. Secondly, use the above AR features to simulate airway insertion including manipulating the controller to insert the cable into the airway, showing inside of the airway from a camera at the tip of the cable.  Finally, use Azure features of Spatial Anchors and Holographic Remoting.

 
**Marking criteria**

The marking criteria are defined in the table below. The content has three categories: basic AR features, simulation features and Azure features.

| <a>Features</a>                                                                 | <a>Percentage (%)</a> |
| :---                                                                            | ---: |
| **Basic AR Features**                                                           |                |
| MRTK initializing and configuring                                               | 10             |
| Positioning objects in the scene                                                | 10             |
| Creating dynamic content using Solvers                                          | 10             |
| Interacting with 3D objects                                                     | 10             |
| Eye tracking                                                                    | 10             |
| Voice commands                                                                  | 10             |
| **Simulation Features**                                                         |                |
| Manipulation of the controller                                                  | 10             |
| Showing inside of the airway from a  camera at the tip of the optical fiber     | 10             |
| **Advanced Features**                                                           |                |
| Spatial Anchors                                                                 | 10             |
| Holographic Remoting                                                            | 10             |
| **Total**                                                                       | 100            |
 
### Implementation

**Basic AR Features**

The basic AR features and Azure features are supported by the lab tutorials. The Simulation features are application of the basic AR features.

- MRTK initializing and configuring

Create a new Unity project configured for MRTK development, and import MRTK. Configure, build, and deploy a basic Unity scene from Visual Studio to your HoloLens 2. Modify a setting in the MRTK profile, e.g. hide/show the spatial awareness mesh by changing the settings of the Spatial Mesh Observe.

- Positioning objects in the scene

Import appropriate assets and position objects in the scene relative to the user and use MRTK's Grid Object Collection feature to organize objects in a collection. Assets include the airway model, the controller and cable model. 

- Creating dynamic content using Solvers

Use the MRTK's Directional Indicator Solver to have a UI element intuitively direct the user to objects, e.g. add a directional indicator to direct the user to the airway model. Use the Tap to Place Solver to reposition objects, e.g. reposition the airway model to another location.

- Interacting with 3D objects

Enable near and far manipulation for 3D objects and limit the allowed types of manipulation. Add Bounds Control around 3D objects to make it easier to control the object manipulation e.g. add a BoundsControl to the controller object so the controller can easily be moved and rotated.

- Eye tracking

Enable eye-tracking for HoloLens 2 and add eye-tracking to objects to trigger actions when the user looks at the objects, e.g. when the user looks at the controller, highlight it or take other actions.

- Voice commands

Create speech commands. A speech command requires the user to look at the object and issue a speech command, e.g. the user look at the controller and say “clockwise” to rotate the controller clockwise. Other similar commands can be “anticlockwise” etc.

**Simulation Features**

- Manipulation of the controller

The user should be able to use hands to translate/rotate the controller and advance/retreat the cable in/out of the airway. The system should detect collisions between the cable and airway walls. The user should use the left hand hold the controller and right hand hold the cable. The right hand should rotate and translate the controller. The left hand should advance and retreat the cable. See examples above.

- Showing inside of the airway from a camera at the tip of the optical fiber

The system should add a camera at the tip of the cable. The user should be able to control the camera to rotate it in a hemispherical range.  The system should show the image of the inside of the airway seeing from the camera. A similar image can be found at Figure 4 in the reference [Casso 2019](https://journals.lww.com/anesthesia-analgesia/fulltext/2019/11000/development_and_initial_evaluation_of_a_novel,.14.aspx).

**Advanced features**

- Azure Spatial Anchors

The system should be able to start and stop an Azure Spatial Anchors session and create, upload, and download Azure Spatial Anchors on a single HoloLens 2 device, e.g. anchor the airway model on the surface of a physical desk or ground.

- Holographic Remoting

Create a Holographic Remoting remote PC app and connect to HoloLens 2 at any point, providing a way to visualize 3D content in mixed reality.

### References

Casso, G., Schoettker, P., Savoldelli, G.L., Azzola, A. and Cassina, T., 2019. Development and initial evaluation of a novel, ultraportable, virtual reality bronchoscopy simulator: the computer airway simulation system. Anesthesia & Analgesia, 129(5), pp.1258-1264.

Agasthya, N., Penfil, S. and Slamon, N., 2020. Virtual Reality Simulation for Pediatric Airway Intubation Readiness Education. Cureus, 12(12).
