# Sunbeam extension sbx_bowtie2_mapping

This is a Sunbeam (https://github.com/sunbeam-labs) extension to map reads back to target genome using bowtie2 global alignment. This is a alternative way for default sunbeam "mapping" method, which use BWM, which based local alignment.

# Installing and running

Activate sunbeam and clone the repo to `sunbeam/extension`
```
source activate sunbeam
cd $SUNBEAM_DIR
git clone https://github.com/guanzhidao/sbx_bowite2_mapping extensions/sbx_bowtie2_mapping
conda install --file extensions/sbx_bowtie2_mapping/requirements.txt
```

Remember to add dedup option to your sunbeam config file
```
cat $SUNBEAM_DIR/extensions/sbx_bowtie2_mapping/config.yml >> $PROJECT_DIR/sunbeam_config.yml
sunbeam run --configfile $PROJECT_DIR/sunbeam_config.yml all_bowtie2_mapping
```

