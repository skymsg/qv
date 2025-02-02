# Usage

## Run query on data

```bash
qv s3://tpc-h-parquet/1/customer -q 'select c_custkey, UPPER(c_name) from tbl'
```

## View schema of data

```bash
qv ./datasets/tpc-h-parquet/1/customer -s
```

## View data on GCS.

```bash
qv gs://datafusion-delta-testing/data/delta/COVID-19_NYT
```

## View data on S3

```bash
qv s3://tpc-h-parquet/1/customer
```

## Specify AWS (SSO) profile to use

```bash
qv s3://tpc-h-parquet/1/customer --profile my-user
```

## View data from S3 console URL

```bash
qv https://s3.console.aws.amazon.com/s3/buckets/datafusion-delta-testing?region=eu-central-1&prefix=simple_table/&showversions=false
``` 

## View data which matches a globbing pattern:

```bash
qv "s3://datafusion-parquet-testing/data/alltypes_pla*n.parquet"
```

## View delta table (no need for a manifest)

```bash
qv /Users/timvw/src/github/delta-rs/rust/tests/data/COVID-19_NYT
```

## View delta table at specific point in time

```bash
qv /Users/timvw/src/github/delta-rs/rust/tests/data/COVID-19_NYT --at "2022-01-01T16:39:00+01:00"
```

## View glue table

```bash
qv glue://mydb.table1
```