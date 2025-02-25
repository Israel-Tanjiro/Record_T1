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
		const G4ThreeVector & tLate, // Iniial Cooodinates (Green point see Figure 1)
		const G4String & pName, // Name of the qubit
             	G4double  LX1,// X dimension must be in microns
             	G4double  LY1,// Y dimensions must be in microns
              	G4double  LX2,// X dimensions must be in microns
              	G4double  LY2,// Y dimensios must be in microns
		G4double  LXG1,// X dimension of the Vaccum Qubit
		G4double  LYG1,// Y dimension of the Vaccum Qubit
		G4double  LXG2,// X dimension of the Vaccum Qubit
		G4double  LYG2,// Y dimension of the Vaccum Qubit
              	G4double Gap, // X dimension of the Vaccum Gap 
		G4LogicalVolume * pMotherLogical, // Place to put the Qubit
		G4bool GroundPlane, // Option to build the Cross Qubit without Vaccum Gap. You must put false
		G4int Refle, // Parameter to put the Cross Qubit above the Y axis. Only 0 or 1 for 1 above of Y axis
		G4bool pMany, // If you want to copy the same geometry
		 G4int pCopyNo, //Number of the Copy
             	G4bool pSurfChk) // To check intersection with other geometries. True or False
```
You can acces to the following attributes Xf and Yf, those are the coordinates of the center of the Cross Qubit (red point Figure 1). You will need those values to do a Phonon Collection Efficiency. This is an example of the initialization of the Class
```cpp
CrossQubit_1 *Qubit1Cr= new CrossQubit_1(0,G4ThreeVector(Xf,Yf,0),"Qubit1Cr",320,25,25,320,0.0,log_GroundPlaneMesh,true,false,0,checkOverlaps);
```
![Workflow Diagram](Cross_Qubit.png)

## Transmission Line
The Class contain the Following Parameters.
```cpp
Tranmission_line::Tranmission_line(G4RotationMatrix * pRot,// To Rotate the Qubit
		const G4ThreeVector & tLate, //Iniial Cooodinates (Green point see Figure 1)
		const G4String & pName,
		G4double  CPWlenght,
             	G4double  CPWWidth,
   		G4double  XRectangle,// Length of Rectangle in X direction
		G4double  YRectangle,// Height of Rectangle in Y direction
             	G4double  Thicknnes,//
		G4double  SBase,
		G4double  HeightTrap,
		G4LogicalVolume * pMotherLogical,
		G4bool GroundPlane,
		G4bool pMany,
		G4int pCopyNo,
		G4bool pSurfChk)

```
![Workflow Diagram](CPw.png)



