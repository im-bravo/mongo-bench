我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。


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
