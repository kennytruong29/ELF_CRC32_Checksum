# CS530Assignment1
Kenny Truong

kennytruong29@yahoo.com

## Prog1_1
### Purpose
Perform a CRC32 checksum on a binary (ELF) file
### Inputs
Name of the ELF file
### Outputs
CRC32 checksum hex value
### Method
Open the binary file, get the size of the Elf file, manipulate bit by bit using the CRC32 algorithm
*Each part uses a CRC table*

## Prog1_2
### Purpose
Perform a CRC32 checksum of the program header of the binary (ELF) file
### Inputs
Name of the ELF file
### Outputs
CRC32 checksum hex value of the program header
### Method
Open the binary file, seek to the file header, seek to the program header,
read the program header and manipulate it bit by bit using CRC32 algorithm


## Prog1_3
### Purpose
Perform a CRC32 checksum of a specific section name of the binary (ELF) file
### Inputs
Name of the ELF file, name of the section (argv[2])
### Outputs
CRC32 checksum hex value(s) of the section header
### Method
Open the binary file, seek to the file header, seek to the section header
string table, get the names. Seek to each section and compare to argv[2].
If section == argv[2], perform CRC32 on its bits.
