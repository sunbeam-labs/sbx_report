# Sunbeam Report extension

This is an extension to generate a visual report from outputs from the [Sunbeam pipeline](https://github.com/sunbeam-labs/sunbeam). 

## Installing

As of Sunbeam version 3.0, simply run:

```sh
sunbeam extend https://github.com/sunbeam-labs/sbx_report sunbeam/extensions/sbx_report
```

Prior to version 3.0, you should manually move or clone the extension directory into the sunbeam/extensions/ folder:

```sh
git clone https://github.com/sunbeam-labs/sbx_report sunbeam/extensions/sbx_report
```

All dependencies are handled by Snakemake and conda at runtime with the `--use-conda` flag.

## Running 

To generate the report, simply add `--use-conda` and specify `final_report` as the target rule:

```sh
sunbeam run --configfile=sunbeam_config.yml --use-conda final_report
```    

(`--use-conda` will tell Snakemake to automatically maintain a separate conda
environment from Sunbeam for this extension, to avoid any package conflicts.)

A self-contained HTML file is generated in your specified output folder under 'reports'.

## Example

Click [here](https://rawgit.com/sunbeam-labs/sbx_report/master/example.html) for an example report.
