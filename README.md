# Sunbeam Report extension

This is an extension to generate a visual report from outputs from the [Sunbeam pipeline](https://github.com/sunbeam-labs/sunbeam). 

## Installing

Installing an extension is as simple as cloning (or moving) your extension directory into the sunbeam/extensions/ folder, installing requirements through Conda, and adding the new options to your existing configuration file: 

```sh
git clone https://github.com/sunbeam-labs/sbx_report sunbeam/extensions/sbx_report
conda install --file sunbeam/extensions/sbx_report/requirements.txt
```

## Running 

To generate the report, simply specify `final_report` as the target rule:

```sh
sunbeam run --configfile=sunbeam_config.yml final_report
```    

A self-contained HTML file is generated in your specified output folder under 'reports'.

## Example

Click [here](https://rawgit.com/sunbeam-labs/sbx_report/master/example.html) for an example report.
