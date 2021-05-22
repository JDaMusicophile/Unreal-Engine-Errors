# Unreal-Engine-Errors
Hey Guys! Thought of providing some help to everyday Unreal Engine Developers, with solutions to everyday issues/errors developers like myself have faced. Feel free to contact me via discord for further help or to provide some of your wise advice. This list will be updated regularly. 


# Deletable Files

The listed are folders that can be deleted safetly from the UE4 game files:

Saved

Config

Source

Intermediate/ProjectFiles

Binaries

After deleting the neccessary, please make sure to regenerate your vs files! 

# Errors

1) "Game_Name" failed to compile. Try building from source manually

    Try deleting the files stated above, and regeneate files. Then build the game via visual studio.

2) A lock file already exists in the repository, which blocks this operation from completing

   navigate to the repo git;
   github desktop - repository/open in git bash
   and type the following command
   `<rm -f .git/index.lock>`

3) InstancedFoliageActor_0 Instanced meshes don't yet support unique static lighting for each LOD. Lighting on LOD 1+ may be incorrect unless lightmap UVs are the same for all LODs.

   - Change LOD group from none to foilage

4) Overlapping Uvs
  
   - Change Mesh mobility from static to stationary or moveable
   - Change UV Channel for each mesh, to none-overlapping 

5) InstancedFoliageActor_0 The total lightmap size for this InstancedStaticMeshComponent is large, consider reducing the component's lightmap resolution or number of mesh instances in this component

   - Go to Foilage mode ->  Instance Settings  -> Lightmap resolution -> Tick on default 8 (Or reduce to what you pleases you)

6) [Actor] has invalid DrawScale/ DrawScale3D
 
   - This warning is caused when either DrawScale, DrawScale3D X, DrawScale3D Y, or DrawScale 3D Z is equal to zero. 
     Meaning that the Actor will not be shown because it is being scaled to zero on one of its axis. 
     To solve this problem, change any DrawScale's that are zero to be non-zero by selecting the Actor and changing its drawscale at the bottom of the main UnrealEd window.

<br />
<br />

# Happy Coding!! :love_you_gesture:


