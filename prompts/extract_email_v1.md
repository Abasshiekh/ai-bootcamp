Prompt 1

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
