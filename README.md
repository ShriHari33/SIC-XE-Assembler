# C++ Assembler Project

This project is my take on the implementation of a `Two-Pass` assembler in C++ for the SIC/XE architecture. The implementation supports all of the `addressing modes` provided by the SIC/XE, along with the `Control Section` machine independent feature.

## First Pass

The `pass1.cpp` file performs the first pass of the assembler. It includes several functionalities:

- It includes the necessary classes and utilities for the assembly process.
- It initializes the operation table (`opTab`) and the register table (`regTab`).
- It reads the Assembly input from the (`input.txt`) file and generates:
    - an intermediate file (`intermediate.txt`)
    - Symbol Table for each Control Section, which are stored as a single collection called 'symTabs'
- Any error encountered during Pass 1 will be mentioned in the intermediate file.

## Second Pass

The `pass2.cpp` file is the second pass of the assembler. It takes in the `intermediate file` & the `symbol Tables` and generates:
- a listing file `listing.txt` that consists of detailed information about each instruction, along with errors if any that were encountered.
- an object file `object.txt` that gets generated **ONLY** if there were no errors during the second pass. This consists of machine code in hexadecimal along with the appropriate records.

## Running the assembler

To run this project, you need:
- `g++ compiler` that can compile atleast the C++11 standard code. You can use any other compiler of your choice, but make sure to change the `MakeFile` appropriately.
- `make` tool.

After you have the above 2 requirements satisfied, just go to the installed directory on your system and type `make` in the terminal.

It will generate you an executable `assembler` that can be invoked by typing `./assembler` in the terminal. It by default takes in the input file `input.txt` & starts from the `pass1.cpp` file.

## Usage

To use this assembler, provide the assembly instructions in the `input.txt` file. The assembler will process these instructions and output the results accordingly.

A sample input.txt file has already been given in the directory which has no errors as far as SIC/XE architecture is concerned with.


## Further Scope

I plan to write more machine independent features such as, `program blocks`, `macro facilities` in the future whenever I get back to working with this.

## Contributing

Contributions are welcome. Please open an issue first to discuss what you would like to change.


## License

This project is licensed under the [Creative Commons Attribution 4.0 International License](LICENSE).
