# Record_T1
## Table of Contents

- [About](#about)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)
## About
This project allow you to simulate phonon transport on G4CMP. The project has libraries to create qubits geometries as: Cross qubits, resonators transmission line and a Meshed ground plane. 
## Cross Qubit Class
The Class contain the followings intial parameters
```cpp
CrossQubit::CrossQubit(G4RotationMatrix * pRot, // To Rotate the Qubit
		const G4ThreeVector & tLate, // Iniial Cooodinates (red point see Figure 1)
		const G4String & pName, // Name of the qubit
             	G4double  LX1,// X dimension must be in microns
             	G4double  LY1,// Y dimensions must be in microns
              	G4double  LX2,// X dimensions must be in microns
              	G4double  LY2,// Y dimensios must be in microns
              	G4double Gap, // X dimension of the Vaccum Gap 
		G4LogicalVolume * pMotherLogical, // Place to put the Qubit
		G4bool GroundPlane, // Option to build the Cross Qubit without Vaccum Gap. You must put false
		G4int Refle, // Parameter to put the Cross Qubit above the Y axis. Only 0 or 1 for 1 above of Y axis
		G4bool pMany, // If you want to copy the same geometry
		 G4int pCopyNo, //Number of the Copy
             	G4bool pSurfChk) // To check intersection with other geometries. True or False
```
You can acces to the following attributes Xf and Yf, those are the coordinates of the center of the Cross Qubit. You will need those values to do a Phonon Collection Efficiency. This is an example of the initialization of the Class
```cpp
CrossQubit *Qubit1= new CrossQubit(rotPart,G4ThreeVector(XQ1,YQ1,0),"Qubit1",400,300,GapQubitX,GapQubitY,0.0,log_GroundPlaneMesh,true,false,0,checkOverlaps);




