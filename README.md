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
		G4LogicalVolume * pMotherLogical,
		G4bool GroundPlane,
		G4int Refle,
		G4bool pMany,
		 G4int pCopyNo,
             	G4bool pSurfChk)
