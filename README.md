
# Mongo Bench

## install
go get github.com/im-bravo/mongo-bench
cd ~/go/bin

## write
```bash
./mongo-bench -workload uniform -mode write -concurrency 1 -duration 2s -nodes 192.168.58.100 -username root -password example -keyspace your_database -table your_table
```

## write and check
## write to first node, and read from second node.
```bash
./mongo-bench -workload uniform -mode write_read -concurrency 1 -duration 2s -nodes 192.168.58.100,192.168.58.101 -username root -password example -keyspace your_database -table your_table
```




####   run original golang (development)
```bash
go run main.go modes.go workloads.go -workload uniform -mode write -concurrency 1 -duration 2s -nodes 192.168.58.100 -username root -password example -keyspace your_database -table your_table
go run main.go modes.go workloads.go -workload uniform -mode write_read -concurrency 1 -duration 2s -nodes 192.168.58.100,192.168.58.101 -username root -password example -keyspace your_database -table your_table
```
