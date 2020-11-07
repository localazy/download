# Localazy Download docker action

Download localizable files from the Localazy translation management platform. For detailed documentation of Localazy CLI, please [visit the documentation](https://localazy.com/docs/cli/the-basics).

## Inputs

### `workdir`

**Optional** Defines the working directory where to invoke Localazy CLI command.

### `config_file`

**Optional** The filename of the configuration file. Default: localazy.json

### `key_file`

**Optional** The filename of the key file.

### `read_key`

**Optional** The read key for the project on Localazy. Can be defined in the config or key file but we recommend to use Github Secrets. 

### `write_key`

**Optional** The write key for the project on Localazy. Can be defined in the config or key file but we recommend to use Github Secrets. 

### `groups`

**Optional** Define groups to be uploaded separated with a space. The default group is always uploaded. If no groups are provided, only the default one is uploaded.

## Example usage

```yaml
uses: localazy/download@v1
with:
  read_key: ${{ secrets.LOCALAZY_READ_KEY }}
  write_key: ${{ secrets.LOCALAZY_WRITE_KEY }}
```
