# Fuzzing

## Get vulnerable source

```bash
git clone https://github.com/fuzzstati0n/fuzzgoat
cd fuzzgoat
```

## Run docker 

```bash
docker run -ti -v /path/to/fuzzgoat:/src aflplusplus/aflplusplus
```
- this mounts the sources of the vulnerable application in the docker image which contains the afl binaries

## Change the directory to the vulnerable application

```bash
cd /src
```

## Build the application with afl && run tests

```bash
make 
make afl
```

## Inspect found crashes afterwards

- normal application execution:
```bash
./fuzzgoat out/default/crashes/errorfilename
```

- extended application error messages
```bash
./fuzzgoat_ASAN out/default/crashes/errorfilename
```

