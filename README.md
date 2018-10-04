# Go standard library benchmarks for all releases from 1.2.2

These benchmarks were created on a GCE dedicated instance of type n1-standard-2 (2 vCPUs, 7.5 GB memory), Intel Haswell, running Debian 9 (stretch).

All benchmarks were run using the command `go test -run=NONE -bench=. ./...` .

To compare the benchmarks do:

```console

$ go get golang.org/x/tools/cmd/benchcmp
$ benchcmp go1.10.linux-amd64-bench.txt go1.11.linux-amd64-bench.txt
```

To vizualize the comparison do:

```console

$ go get github.com/ajstarks/svgo/benchviz
$ benchcmp go1.10.linux-amd64-bench.txt go1.11.linux-amd64-bench.txt  | benchviz > 1.10-1.11.svg
```

DISCLAIMER: These benchmarks are not authoritative, and may not be accurate. They were all created on the same GCE instance, and no other user tasks were run during the creation of them, but variations in the load on the machine may have been caused by Linux sub-systems, scheduled tasks, full moons and gremlins. If you find obvious problems with the results please file a PR and I will attempt to work out what the cause may have been.