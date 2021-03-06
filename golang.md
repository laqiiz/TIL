# Go


## go mod

* `set GO111MODULE=on`
* `go mod init`
* `go build`


## Linter

* `gometalinter`
  * `$FileDir$ --fast --disable=dupl --disable=golint`
  * gometalinter is deperecated!! use [golangci-lint](https://github.com/golangci/golangci-lint)

* golangci-lint
  * 5x faster than gometalinter

* [GolangCI](https://golangci.com/)
  * SaaS Service that using golangci-lint and integrate with GitHub repository.
  * work time is within 1 minute!!

## Debugger error

1. this message occured.
```
could not launch process: decoding dwarf section info at offset 0x0: too short

Debugger finished with exit code 1
```
2. action: `go get -u github.com/derekparker/delve/cmd/dlv`
  * [decoding dwarf section info at offset 0x0: too short
](https://stackoverflow.com/questions/52230503/decoding-dwarf-section-info-at-offset-0x0-too-short)


## Programming Tips

### go-bigquery

* BigQueryへクエリを実行する際のタグ名は `bigquery`。設定しない場合はフィールド名と完全一致。
  * https://godoc.org/cloud.google.com/go/bigquery

```golang
// struct tag is `bigquery`
type Cost struct {
	ProjectName string `bigquery:"project_name,nullable"`
	Day         string `bigquery:"export_time"`
	Cost        int    `bigquery:"cost"`
}

	it, err := r.client.Query(query).Read(context.Background())
	if err != nil {
		return nil, errors.WithStack(err)
	}

	var timeseries []Cost
	for {
		var cost Cost
		err := it.Next(&cost) // must not inline L54!!
		if err == iterator.Done {
			break
		}
		if err != nil {
			log.Printf("Failed to Iterate Query:%v\n", err)
			break
		}
		log.Printf("%v\n", cost)
		timeseries = append(timeseries, cost)
	}
```

https://godoc.org/cloud.google.com/go/bigquery

