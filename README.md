# ICE 5: Basic Elevator Controller

VHDL for ECE 281 [ICE 5](https://usafa-ece.github.io/ece281-book/ICE/ICE5.html)

Targeted toward Digilent Basys3. Make sure to install the [board files](https://github.com/Xilinx/XilinxBoardStore/tree/2018.2/boards/Digilent/basys3).

Tested on Windows 11.

---

## Build the project

You can simply open `elevatorController.xpr` and Vivado will do the rest!

## GitHub Actions Testbench

The workflow uses the [setup-ghdl-ci](https://github.com/ghdl/setup-ghdl-ci) GitHub action
to run a *nightly* build of [GHDL](https://ghdl.github.io/ghdl/).

The workflow uses GHDL to analyze, elaborate, and run the entity specified in the `.github/workflows/testbench.yml`.

```yaml
env:
  TESTBENCH_ENTITY: elevator_controller_fsm
```

If successful then GHDL will quietly exit with a `0` code.
If any of the `assert` statements fail **with** `severity failure` then GHDL will cease the simulation and exit with non-zero code; this will also cause the workflow to fail.
Assert statements of other severity levels, such as "error" w

![image](https://github.com/Parkerb33/ece281-ice5/assets/142423100/f8c3cba5-2117-4d1a-8693-b96e2cd78602)

doc statement
Griffin Greenwood helped me with the code and waveform :)
