# Conda Env Cheat Sheet
### List available environments
```
conda info --envs
```

### Create a new env with specific python version
```
conda create --name env_name python=3.6
```

### Activate specific env
```
source activate env_name
```

### Deactivate specific env
```
source deactivate env_name
```

### Remove a specific env
```
conda remove --name env_name --all
```
