# DP-203_Lab11
# 🚀 Apache Spark Notebook in een Pipeline met Azure Synapse

Welkom bij mijn datapret-avontuur! 🎉 In deze lab heb ik een pipeline gebouwd met een Apache Spark-notebook in Azure Synapse Analytics. Geen saaie code-uitleg, gewoon een gezellige walkthrough van wat ik heb gedaan. Pak een kopje koffie ☕ en lees mee!

---

## 🎯 Wat was het doel?

Een Spark-notebook automatiseren binnen een pipeline in Azure Synapse Analytics. Ja, het klinkt serieus – en dat was het ook een beetje – maar eigenlijk was het vooral leuk om te doen!

---

## 🛠️ Wat heb ik allemaal gedaan?

### 🔧 1. Synapse Workspace opzetten
Met een PowerShell-script en een ARM-template heb ik een hele Synapse-omgeving laten opbouwen. Denk aan een workspace, data lake storage én een Spark pool. Lekker alles automatisch geregeld!

### 🗂️ 2. Data verkennen
In Synapse Studio ben ik naar de 'Data' pagina gegaan, en daar zag ik de CSV-bestanden in een mapje genaamd `data`. Even stiekem een voorproefje genomen via de "Preview"-functie. 😏

### 📒 3. Notebook draaien
Een notebook genaamd **Spark Transform.ipynb** gedownload van GitHub (die link met die drie puntjes, you know 😉). Vervolgens:
- Geïmporteerd in Synapse Studio
- Verbonden met mijn Spark pool
- Alles lekker handmatig uitgevoerd met "Run All"

Het resultaat? Getransformeerde data in Parquet-formaat, netjes opgeslagen in een unieke map.

### 📈 4. Data bekijken in SQL
Even snel een top 100 SQL-query losgelaten op de nieuwe Parquet-bestanden. Alles netjes getransformeerd. YES! ✅

---

## 🔁 Automatiseren met een Pipeline

### 💡 Parameter ingesteld
De eerste cel van het notebook als *parameter cell* gemarkeerd. Zo kon ik straks vanuit de pipeline de foldernaam dynamisch instellen.

### 🧩 Pipeline gebouwd
- Nieuwe pipeline aangemaakt: **Transform Sales Data**
- Een Notebook activity toegevoegd
- Parameter `folderName` ingesteld op `@pipeline().RunId`
- Spark pool aangesloten
- Alles netjes gepublished

### ▶️ Pipeline uitgevoerd
Met één klik op "Trigger now" begon de magie. Na een paar minuutjes… BAM 💥 Nieuwe folder in de storage, gevuld met Parquet-bestanden van de getransformeerde data.

---

## 🧹 Opruimen maar
Na afloop netjes de resource group verwijderd via de Azure Portal. Clean as a whistle!

---

## ✨ Wat heb ik geleerd?

- Werken met Synapse Pipelines en Spark notebooks is eigenlijk best leuk!
- Automatiseren van datatransformaties voelt magisch 🪄
- En ja, zelfs PowerShell kan handig zijn 😅

---

> Bedankt voor het lezen van mijn mini-avontuur in de wereld van Azure Data Engineering. 💙
>
> 
![Schermafbeelding 2025-04-15 104400](https://github.com/user-attachments/assets/5f90995e-6de5-42c8-ae9f-2177bc78624a)
![Schermafbeelding 2025-04-15 105050](https://github.com/user-attachments/assets/5ea4f86b-fc05-45ab-924a-cab0c71df3e9)
![Schermafbeelding 2025-04-15 113224](https://github.com/user-attachments/assets/62af5ecd-7fe3-40f3-80e8-41a2cdb12ca8)
![Schermafbeelding 2025-04-15 123152](https://github.com/user-attachments/assets/6289a25f-7245-40b7-bf61-71b11e58f464)









