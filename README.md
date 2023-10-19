# PIZZA ORDERING CHATBOT

Simple lex chatbot for customer to order pizza

# Steps
1. Navigate to Lex
2. Create a bot
    - Create blank bot
    - Enter Bot name
    - Under IAM pERMISSIONS
        - SELECT CREATE AROLE WITH amazon lex
    - Under Children’s Online Privacy Protection Act (COPPA)
        - Choose No
    - Click Next
    - Slect Language
    - Coose Voice Interaction
    - Click Done

    - Intent: New Intent
        - Intent Details
            - Enter "Order Pizza as Intent nae
        - Add Sample utterances (utterances, are what the user can use to start interaction with the chatbot)
            - Type an Utterance eg hello, hi
            - Click Add utterance
        - Toggle "Confirmation" to active
        - Same with Closing response
        - Under Confirmation, 
            - enter the following in the confirmation prompt:
                "Can I go ahead with your request?"
            - enter the follwing in the decline prompt:
                "Okay, your request will not be submitted."
        - 
        - Under Closing response
            - enter the message as: (response chatbot will give when the user starts interacting with their utterances)
                Hello! Welcome to PizzaHouse. Would you like to order a pizza?
            - (Optional) can add variations to spice things up
                - Click "More responses under Variations
                    - The closing message editor will pop up 
                    - Click on the variations dropdown and enter "Hi there! I'm the PizzaHouse bot. Would you like to order a pizza?"
                    - Click Update responses
        - Save Intent

        * Slots are placeholders for the user input

        - Navigate back to intents list
        - In the Amazon Lex menu, click "slot types" under OrderPizza
            -Click Add slot type dropdown
                - Click "add blank slot type"
            - Specify Slot type name
                - Enter "PizzaType" as Slot type name
                - Click Add
            - Under Slot value resolution
                - Select "Restrict slot values"
            - Under slot type values
                - Under value, enter "Italian"
                - for its corresponding values, enter italian, italy,Italy
                * click tab or ; after each value, for a new one
                - You can add more values like "Mexican", with corresponding values like "mexico", "mexican" etc
            - Save Slot type

            - Navigate back to Slot types
                - Create two more: PizzaCrust and Appetizer

        - Navigate back to Intent: OrderPizza
        - Slots
        - Add slot
            1. Name: Name
                Slot type: AMAZON.firstname
                Prompts: Hello! May I know your first name
        - Click add
        - add more slots:
            - Pizza Type
                - name: PizzaType
                - slot type: pizzatype
                - prompts: {Name}, What pizza would you like to order? 

            * Add custom value by putting the slot name in {} eg {Name}

        - scroll up to Conversational flow to see how the conversation will go

        - Save intent

        - Improve UI by adding values
            - Choose DeliveryTime option
                - click advanced options
                - scroll down to slot prompts
                - click bot elicits information DROPDOWN
                - cLICK more prompt options
                - toggle previow
                -click add
                    -add card group
                    - update card
                        - enter title as "Available times" as placeholder
                        - click buttons fropdown
                            click add button
                                - button 1 title : 20:00
                                - button 1 value : 8pm

                                - button 2 title : 20:30
                                - button 2 value : 8:30pm
                    - click "update prompts"
                    - click update slot
        
        - Save intent

        - Click Build

        - Test



                
