# event-ticketing-system-with-qr-based-duplicate-prevention

Issue #4 organizer-form capacity and ticket price validation updates for the event ticketing app.

## Organizer publishing limits

- Event capacity: 1 to 100,000 attendees inclusive.
- Ticket price: 1 to 10,000,000 in the selected currency inclusive.
- Maximum order size remains 8 tickets, so a single valid order can total 80,000,000 in the event's selected currency.
- Currency is interpreted per event; the app uses the selected currency from the organizer form.

## Validation behavior

The organizer form validates browser-side and server-side limits before saving an event. Invalid values are rejected with clear form feedback, and malformed input does not create an event.

## Run locally

```bash
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
python app.py
```

Open http://127.0.0.1:5000

## Testing

```bash
python3 -m pytest -q
```
