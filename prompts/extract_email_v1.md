#Prompt 1 Missing Order Number in the email

You are a data-extraction assistant for a small business.

Extract fields from the customer email below. Rules:

  - Return ONLY valid JSON, no extra text.
  - If a field is not stated, use null. Never guess.
  - "urgency" must be one of: "low", "medium", "high".

Schema: {"customer_name": string|null, "order_id": string|null, "issue": string,
"urgency": "low"|"medium"|"high"}

Example input: "Hi, Ravi here. Order 4521 arrived broken, need a replacement
ASAP." Example output: {"customer_name":"Ravi","order_id":"4521","issue":"Item
arrived broken","urgency":"high"}

Email: """ Hi, Abas here. taking long to arrive, need to cancel ASAP """

#Results 

{"customer_name": "Abas", "order_id": null, "issue": "Taking long to arrive, need to cancel", "urgency": "high"}


#Prompt 2 Complete Information provided in the Email. 

You are a data-extraction assistant for a small business.

Extract fields from the customer email below. Rules:

  - Return ONLY valid JSON, no extra text.
  - If a field is not stated, use null. Never guess.
  - "urgency" must be one of: "low", "medium", "high".

Schema: {"customer_name": string|null, "order_id": string|null, "issue": string,
"urgency": "low"|"medium"|"high"}

Example input: "Hi, Ravi here. Order 4521 arrived broken, need a replacement
ASAP." Example output: {"customer_name":"Ravi","order_id":"4521","issue":"Item
arrived broken","urgency":"high"}

Email: """ Hi, Abas here. order no 3221 taking long to arrive, need to cancel ASAP """


#Results 2
{"customer_name": "Abas", "order_id": "3221", "issue": "Taking long to arrive, need to cancel", "urgency": "high"}

#Prompt 3

You are a data-extraction assistant for a small business.

Extract fields from the customer email below. Rules:

  - Return ONLY valid JSON, no extra text.
  - If a field is not stated, use null. Never guess.
  - "urgency" must be one of: "low", "medium", "high".

Schema: {"customer_name": string|null, "order_id": string|null, "issue": string,
"urgency": "low"|"medium"|"high"}

Example input: "Hi, Ravi here. Order 4521 arrived broken, need a replacement
ASAP." Example output: {"customer_name":"Ravi","order_id":"4521","issue":"Item
arrived broken","urgency":"high"}

Email: """ Hi,  here. order no 3221 taking long to arrive, need to cancel ASAP """

#Results 3
{"customer_name": null, "order_id": "3221", "issue": "Order taking long to arrive, need to cancel", "urgency": "high"}


#Prompt 4
You are a data-extraction assistant for a small business.

Extract fields from the customer email below. Rules:

  - Return ONLY valid JSON, no extra text.
  - If a field is not stated, use null. Never guess.
  - "urgency" must be one of: "low", "medium", "high".

Schema: {"customer_name": string|null, "order_id": string|null, "issue": string,
"urgency": "low"|"medium"|"high"}

Example input: "Hi, Ravi here. Order 4521 arrived broken, need a replacement
ASAP." Example output: {"customer_name":"Ravi","order_id":"4521","issue":"Item
arrived broken","urgency":"high"}

Email: """ Hi, abas here. order no 3221 disgusting taking too long to arrive, need it immediately ASAP
"""

#Result 4
{"customer_name": "abas", "order_id": "3221", "issue": "Order taking too long to arrive", "urgency": "high"}
