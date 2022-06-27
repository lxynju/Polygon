# Steps
blockMesh                     # Create a background block
surfaceFeatureExtract         # Extract features
snappyHexMesh                 # Snappy the geometry from background
topoSet                       # Define the boudaries
setExprFields                 # Set Initial surface displacement
decomposePar                  # Divide 80 regions for parallel computation 
bsub < interFoam.sh           # send to HPC system and run
