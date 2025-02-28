## VHDL Source Folders


### [`core`](https://github.com/stnolting/neorv32/tree/master/rtl/core)

This folder contains the core VHDL files for the NEORV32 CPU and the NEORV32 Processor.
When creating a new synthesis/simulation project make sure that all `*.vhd` files from this folder are added to a
*new design library* called `neorv32`.


### [`processor_templates`](https://github.com/stnolting/neorv32/tree/master/rtl/processor_templates`)

Contains pre-configured "SoC" templates that instantiate the processor's top entity from `core`.
These templates can be instantiated directly within a FPGA-specific board wrapper.


### [`system_integration`](https://github.com/stnolting/neorv32/tree/master/rtl/system_integration`)

Top entities in this folder provide the same peripheral/IO signals and configuration generics as the default
processor top entity from `core`, but feature a different interface type.
For example: an **AXI4-Lite**-compatible bus interface instead of the default Wishbone bus interface
or a top entity with _resolved_ port signal types.


### [`test_setups`](https://github.com/stnolting/neorv32/tree/master/rtl/test_setups`)

Minimal test setups (FPGA- and board-independent) for the processor. See the
[README](https://github.com/stnolting/neorv32/tree/master/rtl/test_setups)
in that folder for more information. Note that these test setups are used in the
[NEORV32 USer Guide](https://stnolting.github.io/neorv32/ug).
