# CoreDSL-Instruction-Set-Description of RISC-V

Instruction set description of the RISC-V standard extensions in CoreDSL2.

Arithmetic results are explicitly converted at architectural register and
memory boundaries. These conversions express RISC-V word truncation and
signed/unsigned bit reinterpretation; intermediate multiply widths remain
parameterized by `MUL_LEN`. Floating-point boxing uses masks sized by `FLEN`,
and masks wider than 32 bits have 64-bit unsigned declarations.

The descriptions are checked with M2-ISA-R's `--infer-types --validate` for
RV32 and RV64 ETISS cores. ETISS support definitions and instruction execution
regressions are maintained by the consuming `CoreV_ISA_CoreDSL` repository.
