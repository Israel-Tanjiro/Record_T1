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
CrossQubit::CrossQubit(G4RotationMatrix * pRot,
		const G4ThreeVector & tLate,
		const G4String & pName,
             	G4double  LX1,
             	G4double  LY1,
              	G4double  LX2,
              	G4double  LY2,
              	G4double Gap,
		G4LogicalVolume * pMotherLogical,
		G4bool GroundPlane,
		G4int Refle,
		G4bool pMany,
		 G4int pCopyNo,
             	G4bool pSurfChk)
