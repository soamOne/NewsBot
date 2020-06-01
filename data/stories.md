## getNews happy path 1
* request
    - get_news
    - form{"name": "get_news"}
    - slot{"requested_slot": "key"}
* form: choose{"key": "sports"}
    - slot{"key": "sports"}
    - form: get_news
    - slot{"key": "sports"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - action_restart

## thankyou (general)    
* thank_you
    - utter_welcome


## greet (general)
* greet
    - utter_hello

## getNews happy path 2
* request{"key": "astronomy"}
    - slot{"key": "astronomy"}
    - get_news
    - form{"name": "get_news"}
    - slot{"key": "astronomy"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - action_restart

## getNews happy path 3
* request{"key": "physics"}
    - slot{"key": "physics"}
    - get_news
    - form{"name": "get_news"}
    - slot{"key": "physics"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - action_restart




## say goodbye
* goodbye
  - utter_goodbye



## interactive_story_1
* greet
    - utter_hello
* request{"key": "linkedin"}
    - slot{"key": "linkedin"}
    - get_news
    - form{"name": "get_news"}
    - slot{"key": "linkedin"}
    - slot{"key": "linkedin"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - action_restart

## interactive_story_2
    - get_news
    - form{"name": "get_news"}
    - slot{"requested_slot": "key"}
* form: request{"key": "cars"}
    - slot{"key": "cars"}
    - form: get_news
    - slot{"key": "cars"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - action_restart

## interactive_story_1
* greet
    - utter_hello
* goodbye
    - utter_goodbye

## interactive_story_1
* greet
    - utter_hello
* request
    - get_news
    - form{"name": "get_news"}
    - slot{"requested_slot": "key"}

## interactive_story_2
* greet
    - utter_hello
* request{"key": "AI"}
    - slot{"key": "AI"}
    - get_news

## interactive_story_3
* greet
    - utter_hello
* request{"key": "AI"}
    - slot{"key": "AI"}
    - get_news
    - form{"name": "get_news"}
    - slot{"key": "AI"}
    - slot{"key": "AI"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - action_restart

## interactive_story_4
* greet
    - utter_hello
* request{"key": "sports"}
    - slot{"key": "sports"}
    - get_news
    - form{"name": "get_news"}
    - slot{"key": "sports"}
    - slot{"key": "sports"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - utter_confirm_if_service_is_correct
* affirm
    - action_restart

## interactive_story_5
* request{"key": "tech"}
    - slot{"key": "tech"}
    - get_news
    - form{"name": "get_news"}
    - slot{"key": "tech"}
    - slot{"key": "tech"}
    - form{"name": null}
    - slot{"requested_slot": null}
    - utter_confirm_if_service_is_correct
* affirm
    - utter_welcome
* goodbye
    - utter_goodbye
