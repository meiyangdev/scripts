```
cat ~/.aws/config
CSV.open("/tmp/test.csv", "w") do |csv|
  csv << ['Name', 'Roles', 'Created At', 'Updated At']
  admin_users.each do |user|
    csv << [user[0], user[1], user[2], user[3]]
  end
end

aws s3api list-buckets
aws s3 cp ./test.csv s3://temporary-storage-bucket/test.csv 
aws s3 ls s3://temporary-storage-bucket
```

generate CSV
```
report_csv = CSV.generate(headers: true) do |csv|
  user_data.each do |row|
  csv << row
  end
end
```
