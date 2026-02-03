---
description: Send data to the model, and listen to events sent from the model
---

# Events & Listeners

You can send data to the model, and also listen to events dispatched from the model.



## Api Events



```typescript
enum ApiEvents 
	INTERACTION_CUSTOM_EVENT = "{custom_event_name}",
	MOUSE_MOVE = "mouse_move",
	MOUSE_DRAG = 'mouse_drag',
	MOUSE_DOWN = "mouse_down",
	MOUSE_UP = 'mouse_up',
	MOUSE_CLICK = "mouse_click",
	MOUSE_WHEEL = 'mouse_wheel',
	KEY_DOWN = 'key_down',
	HOVERED_OBJECT = 'hovered_object',
	CONFIGURATOR_STATE_CHANGE = "configurator_state_change",
	SELECTION_STATE_CHANGE = "configurator_state_change",
}
```



## Event Responses



Custom events need to be setup directly in studio.



`configurator_state_change`

```typescript
return ConfigurationState[]
```



## Add event listener



&#x20;[addeventlistener.md](api-reference/addeventlistener.md "mention")



## Remove event listener&#x20;

\
[removeeventlistener.md](api-reference/removeeventlistener.md "mention")



## Dispatching Custom Events



[dispatchevent.md](api-reference/dispatchevent.md "mention")<br>





