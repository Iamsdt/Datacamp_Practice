#### conda search

```
conda search numpy => serch all numpy version
```

#### conda list

```
conda list numpy => seach installed version
conda list => all installed version
conda list 'numpy|pandas' > show installed version of numpy and pandas
```

#### -c / -channel

```
conda install --channel my-organization the-package
conda install --channel conda-forge youtube-dl
```

#### env

```
conda env list => show list of environment
conda list --name pd-2015 'numpy|pandas' => show numpy and pandas version in pd-2015 env
```

##### Activation and deactivation

```
conda activate course-env
```

```
conda deactivate => deactivate current environment
```

#### remove environment

```
conda env remove --name deprecated => remove deprecated env
```

#### Create

```
conda create --name recent-pd python=3.6 pandas=0.22 scipy statsmodels => create env recent-pd and install pandas, scipy and statsmodels

conda create --name test => create test env
```

#### Export

```
conda env export -n course-env --file course-env.yml => save into course-env.yml file
conda env export -n course-env => export the list of env
```

#### recreate

```
conda env create --file environment.yml => recreate the environment
conda env create --file environment.yml -n shared-project => recreate environment with name
```