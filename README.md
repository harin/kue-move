# kue-move

Move kue jobs to different states from the command-line

```
  Usage: kue-move [options]

  Options:

    -h, --help              output usage information
    -V, --version           output the version number
    -f, --from <fromState>  From state
    -t, --to <toState>      To State
    -j, --job [jobType]     Job Type Condition
    -a, --age [jobAge]      Job Age Condition
    -v, --verbose
```


## Installation
```
npm install -g kue-move
```

## Usage
requeue stuck jobs
```
$ kue-move --from active --to inactive
```

requeue stuck job for a specific type
```
$ kue-move --job jobName --from active --to inactive
```

move all active jobs to fail
```
$ kue-move --from active --to failed
```


## TODOs
- [ ] implement age condition
- [ ] add test
