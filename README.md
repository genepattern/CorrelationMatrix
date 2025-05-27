# CorrelationMatrix

**Description**: This GenePattern module calculates the correlation matrix from a GCT file using the specified correlation method and dimension.

**Authors**: Edwin Huang, Aditya Kakarla, Razeen Khan

**Contact**: [Forum Link](https://groups.google.com/forum/?utm_medium=email&utm_source=footer#!forum/genepattern-help)

## Summary

This module computes the correlation matrix of a given GCT file. It supports Pearson, Spearman, and Kendall correlation methods and can compute correlations between either columns or rows of the input data. The module uses the [genepattern-python library](https://github.com/genepattern/genepattern-python) to read and write GCT files, making it compatible with GenePattern's standard file formats. Users can specify the input GCT file, the correlation method, and the dimension (rows or columns) to analyze, and the module outputs the resulting correlation matrix in GCT format.

## Source Links

* [The GenePattern CalculateCorrelationMatrix v1 source repository](https://github.com/genepattern/CorrelationMatrix)

## Parameters

| Name          | Description                                           | Default Value |
|---------------|-------------------------------------------------------|---------------|
| input *       | Input GCT file path                                   |               |
| method        | Correlation method: 'pearson', 'spearman', or 'kendall' | pearson       |
| dimension     | Dimension to correlate: 'column' or 'row'             | column        |
| output *      | Output GCT file name                                  | input filename| 

\* required

## Input Files

1. **input**  
   A GCT file containing the data for which to compute the correlation matrix. The GCT file should be in the standard GenePattern GCT format, with rows representing genes and columns representing samples (or vice versa, depending on the analysis). This file is read using the genepattern-python library.

## Output Files

1. **<input_basename>_corr.gct**  
   The correlation matrix in GCT format. If the dimension is set to "column", this file contains correlations between columns of the input data; if set to "row", it contains correlations between rows. Default file name is derived from the name of the input file.

## Example Data

**Input:**  
[example_input.gct](https://github.com/genepattern/CorrelationMatrix/blob/develop/data/example_input.gct)

**Output:**  
[example_output.gct](https://github.com/genepattern/CorrelationMatrix/blob/develop/data/example_output.gct)

## License

`CorrelationMatrix` is distributed under a modified BSD license available at [https://github.com/genepattern/CorrelationMatrix/blob/develop/LICENSE](https://github.com/genepattern/CorrelationMatrix/blob/develop/LICENSE)

## Version Comments

| Version | Release Date | Description                       |
|---------|--------------|-----------------------------------|
| 1       | 2/26/2025       | Initial version of the module.    |
