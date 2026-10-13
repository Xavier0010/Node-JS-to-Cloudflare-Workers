(sesuaikan parameter id dengan record yang di create)

**READ**

> Invoke-RestMethod -Uri "https://paas-express-worker.xavierenochforstudies.workers.dev/api/students" -Method GET

**CREATE**

> $body = @{ name = "Siswa Demo A"; class_name = "XI SIJA" } | ConvertTo-Json
> Invoke-RestMethod -Uri "https://paas-express-worker.xavierenochforstudies.workers.dev/api/students" -Method POST -ContentType "application/json" -Body $body

**UPDATE**

> $body = @{ name = "Siswa Demo B"; class_name = "XI SIJA" } | ConvertTo-Json
> Invoke-RestMethod -Uri "https://paas-express-worker.xavierenochforstudies.workers.dev/api/students/{id}" -Method PUT -ContentType "application/json" -Body $body

**DELETE**

> Invoke-RestMethod -Uri "https://paas-express-worker.xavierenochforstudies.workers.dev/api/students/{id}" -Method DELETE