# Telegram bot to manage [seedr](https://seedr.cc) account

Bot Link: [@TorrentSeedrBot](https://t.me/torrentSeedrBot)

Discussion Group: [@H9Discussion](https://t.me/h9discussion)

---

## ⚒️ Deployment

* Clone the repository, create a virtual environment, and install the requirements

    ```bash
    git clone https://github.com/sarfarazstark/torrhuntbot && virtualenv env && source env/bin/activate && cd torrhuntbot && pip install -r requirements.txt
    ```

* Host the [Torrents-API](https://github.com/Ryuk-me/Torrents-Api) on your own server for better performance or leave it default. This API will be used for inline query only.

* Edit the [src/sample-config.json](src/sample-config.json) file and rename it to `config.json`
* Update bottoken and userId, user https://t.me/userinfobot to get your userid.

    <details>
    <summary>⚙️ Click here to see a sample config file</summary>
    
    ```json
    {
    "botToken": "<BOT Token>",

    "connectionType": "polling",

    "webhookOptions":{
        "webhookHost": null,
        
        "webhookPort": null,
        
        "webhookListen": "0.0.0.0",
        
        "sslCertificate": null,
        
        "sslPrivateKey": null
    },
    
    "adminId" : "<Admin UserId>", 

    "database": "torrenthunt.sqlite",

    "magnetDatabase": "magnets.sqlite",

    "cache": "cache",

    "cacheTime": 86400,

    "language": "language.json",

    "apiLink": "https://torrents-api.ryukme.repl.co/api" 
    }
    ```
    </details>

* Run the [migration.py](migrations.py) file to open a database.

    ```python
    python migrations.py
    ```
* Now, start the bot polling

    ```python
    python torrenthunt.py
    ```

---

Made using [seedrcc](https://pypi.org/project/seedrcc) [https://github.com/hemantapkh/seedrcc]

Author/Maintainer: [Hemanta Pokharel](https://github.com/hemantapkh)
