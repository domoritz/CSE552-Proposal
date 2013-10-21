# All
The data is one file containing the definition of events and a list of operators. For now, we don't care about fragments or workers.

```json
{
	"begin": 123234324,
	"now": 78923492,
	"event_types": [],
	"operators": []
}
```

# Event types

Event types defines single events (happening at one time) and combined events (with begin and end).

```json
{"event_types": [{
		"name": "wait",
		"id": 1
	}, {
		"name": "work",
		"id": 2
	}, {
		"name": "signal",
		"id": 3
	}]
}}
```

# Operators

Contains the actual data.


```json
{"operators": [{
	"type": "JOIN",
	"name": "LocalHashJoin",
	"events": {
		"combined": [{
			"type": 1,
			"begin": 1382298631,
			"end": 1382286341
		}, {
			"type": 2,
			"begin": 1382298812,
			"end": null
		}],
		"single": [{
			"time": 1382298631,
			"type": 3
		}]
	}
}]}
```