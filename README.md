
# Mongo Bench

## install
```sh
go get github.com/im-bravo/mongo-bench
cd ~/go/bin
```

## write
```sh
./mongo-bench -workload uniform -mode write -concurrency 1 -duration 2s -nodes 192.168.58.100 -username root -password example -keyspace your_database -table your_table
```

## write and check
## write to first node, and read from second node.
```sh
./mongo-bench -workload uniform -mode write_read -concurrency 1 -duration 2s -nodes 192.168.58.100,192.168.58.101 -username root -password example -keyspace your_database -table your_table
```




####   run original golang (development)
```sh
go run main.go modes.go workloads.go -workload uniform -mode write -concurrency 1 -duration 2s -nodes 192.168.58.100 -username root -password example -keyspace your_database -table your_table
go run main.go modes.go workloads.go -workload uniform -mode write_read -concurrency 1 -duration 2s -nodes 192.168.58.100,192.168.58.101 -username root -password example -keyspace your_database -table your_table
```
