# All
The data is one file containing the definition of events and a list of operators. For now, we don't care about fragments or workers.

```json
{
	"event_types": {},
	"operators": []
}
```

# Event types

Event types defines single events (happening at one time) and combined events (with begin and end).

```json
{"event_types": {
	"combined": [{
		"name": "wait",
		"begin": {
			"id": 1
		},
		"end": {
			"id": 2,
		}, {...}],
	"single": [{
		"name": "signal",
		"id": 3
	}, {...}]
}}
```

# Operators

Contains the actual data.


```json
{"operators": [{
	"type": "JOIN",
	"name": "LocalHashJoin",
	"events": [{
		"type": 1,
		"timestamp": 1382298631
	}, {
		"type": 2,
		"timestamp": 1382298812
	}]
}]}
```