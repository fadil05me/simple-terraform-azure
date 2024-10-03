# Terraform Script to Create Azure VM

1. Install Terraform
2. Install Azure CLI
3. Login into your Azure using Azure CLI
4. Change ```subscription_id``` on ```main.tf``` and change ```vars.tf``` according to your needs
5. Initialize using ```terraform init```
6. Check the plan ```terraform plan```
7. To start creating use ```terraform apply```

<hr>
<br><br><br>


## Install Terraform
Untuk cara installnya bisa dilihat [DISINI](https://developer.hashicorp.com/terraform/install?product_intent=terraform).

Untuk ubuntu, cara installnya cukup dengan menjalankan command berikut:
```
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

sudo apt update && sudo apt install terraform
```

<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/47fbbe5a-0946-4a63-a2a6-94ce81e7f60f" width="70%"/>

## Install Azure CLI

Install Azure CLI di ubuntu dengan menjalankan command berikut atau untuk OS yang lainnya [DISINI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt):
```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```

<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/347f373d-6429-4436-b54e-34988e70e1bd" width="70%"/>
<br><br><br>

Jika sudah diinstall, login ke azure dengan menjalankan command berikut:
```
az login --use-device-code
```

<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/1e5e2673-8a97-4fe0-8ade-d047e7d1a5e4" width="70%"/>
<br><br><br>


Selanjutnya pergi ke alamat tersebut dengan browser dan pastekan kodenya.

<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/ecfb82ff-6f3a-4fb5-915a-4db6b773a1f2" width="45%"/>
<br><br><br>
Nanti akan muncul seperti ini, disini saya hanya ada 1 subscription. Jadi saya pilih no.1
<br>
<br>
<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/5dc5bab4-5024-4555-ab89-5107e50d8000" width="70%"/>
<br><br><br>

Jika sudah, cek apakah akunnya sudah terhubung.
```
az account show
```

Nanti hasilnya seperti ini:
<br><br>
<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/a095bb43-c63d-4c85-9baa-1ccf9cc4eeec" width="70%"/>
<br><br><br>

Selanjutnya, jalankan command berikut:
```
terraform init;
terraform plan;
```
<br>
Nanti akan muncul seperti ini:
<br><br>
<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/0204e782-6bb7-4422-abfe-1cc21e8a9b8c" width="70%"/>
<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/894fe463-2961-4ab6-8b13-c41d2351f6fd" width="70%"/>
<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/417dad94-844a-44ab-bf16-ffd28a3e36b6" width="70%"/>

<br><br><br>

Jika sudah, jalankan command:

```
terraform apply
```

<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/b9f1ff23-d79a-4731-b02f-6a4f9be126e7" width="70%"/>
<br><br><br>
Jika sukses, nanti akan muncul seperti ini:
<br>
<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/7ea6860f-ca6d-4327-88c8-7f1869065285" width="70%"/>
<br><br><br>
Cek di Dashboard Azure:
<br><br>
<img src="https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/assets/45775729/6c77f613-9e8b-4e4f-94e5-3f39995925cb"/>
<br><br><br><br>


