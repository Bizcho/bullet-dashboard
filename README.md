# BulletDashboard

[toc]

## Entity Relation

```mermaid
erDiagram
	Entry ||--|| Style : "has a"
	Status || --|| Style : belongs
	Entry |o -- o| Status : "has"
	Entry{
		int id PK "Identificador de Entry"
		TimeStamp new_or_update
		string content
		int style FK "Relacion con Style"
		int status FK "Relacion con Status. Nullable"
	}
	Status{
		int id PK "Identificador de Entry"
		string Name
		string bullet
		string format
		int sytle FK "Stule en el que esta permitido el status"
	}
	Style{
		int id PK "Identificador de Entry"
		string name
		string bullet
	}
```

