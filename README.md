# go-18n-sample

** Usage

```
go run main.go

Open http://localhost:8084

Uses github.com/nicksnyder/go-i18n/v2/i18n

```

** Sample language

```json
{
    "hello_world": "Hello World",
    "HelloPerson": {
        "description": "Greet Person",
        "one": "Greeting {{.Name}}",
        "other": "Greeting {{.Name}}"
    },
    "invoices": {
        "description": "The number of invoices a person has",
        "one": "You can {{.Count}} invoice",
        "other": "You have {{.Count}} invoices"
    },
    "messages": {
        "description": "The number of messages a person has",
        "one": "{{.Name}} has {{.Count}} message.",
        "other": "{{.Name}} has {{.Count}} messages."
    }
}
```

**  Code sample

```golang
		helloPerson := localizer.MustLocalize(&i18n.LocalizeConfig{
			DefaultMessage: &i18n.Message{
				ID: "HelloPerson",
			},
			TemplateData: map[string]interface{}{
				"Name": name,
			},
		})
```
