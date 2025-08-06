# spgraph-client
[![PyPI](https://img.shields.io/pypi/v/pbipandas.svg)](https://pypi.org/project/pbipandas/)

**spgraph-client** is a Python client for performing SharePoint actions via Microsoft Graph API like download files, SharePoint list or upload files.

## 📦 Installation
```bash
pip install spgraph-client
```

## 🔧 Usage
```python
from spgraph_client import SharePointClient

client = SharePointClient(
    tenant_id="YOUR_TENANT_ID",
    client_id="YOUR_CLIENT_ID",
    client_secret="YOUR_CLIENT_SECRET",
    site_domain="companyName.sharepoint.com",
    site_name="siteName"
)

# Download a file from SharePoint folder
client.download_file(sp_file_path="Reports", local_path="local_report.xlsx")
# Download all files from a SharePoint folder
client.download_all_files(sp_file_path="Reports", local_dir="local_report")
# Download all files contains a keywords from a SharePoint folder
client.download_files_with_keyword(sp_file_path="Reports",keyword="local_report.pdf",local_dir="local_report")
# Upload file to SharePoint folder
client.upload_file(sp_folder_path="Reports", local_file_path="local_report.pdf")

```
## 📄 License

[MIT License](LICENSE)

---

## 🙌 Contributing

Pull requests are welcome! Please open an issue first to discuss what you would like to change.

---

## ✨ Reference