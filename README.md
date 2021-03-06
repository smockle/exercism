# exercism

Solutions to exercises at exercism.io

## Setup

```Bash
# Build and tag image
$ docker build . --build-arg EXERCISM_API_KEY="${EXERCISM_API_KEY}" -t exercism

# Create and run one-off container
$ docker run -v ~/Developer/exercism:/root/exercism -it --rm exercism
```

## Usage

```Bash
# Fetch next exercise
$ docker run -v ~/Developer/exercism:/root/exercism -w /root/exercism -it --rm exercism fetch swift

# Start next exercise
$ cd ~/Developer/exercism/swift/EXERCISE
$ swift package generate-xcodeproj
$ open EXERCISE.xcodeproj

# Submit current exercise
$ docker run -v ~/Developer/exercism:/root/exercism -w /root/exercism -it --rm exercism submit swift/EXERCISE/Sources/EXERCISE.swift
```

## License

- All files in `Sources` directories, the Dockerfile, and this README.md are licensed under the terms of [LICENSE](LICENSE)
- All other files are licensed under the terms of [exercism/exercism.io LICENSE](https://github.com/exercism/exercism.io/blob/master/LICENSE)
