# ticket-booking-app
a ticket booking app for event attendee and event owners

# Ticket app requirement

1. Users should be able to search for events and buy ticket.
2. Admin should be able to publish event.
3. Ticket should have ticketTypes (VIP/regular) and status (available/ sold-out)
4. Ticket should have verifications (qrCode & number).
5. Event staff should be able to verify tickets at the entrance.

# Nice to have but not yet necessary
6. Payment gateway service to handle user payment
7. Notications should be sent to users when ticket is purchased.

# Non - requirement
1. Authentication and authorization.
2. Enable locking when ticket remains one.

# Main Application Flow
# Flow A — Publish an event
1. Admin creates an event.
2. Admin adds Regular and VIP ticket types, prices, and quantities.
3. Admin publishes the event.
4. The event becomes searchable by users.

# Flow B — Purchase a ticket
1. User searches for an event.
2. User selects a ticket type.
3. Backend checks availability and creates the ticket.
4. Backend generates a unique ticket number and QR token.
5. User receives the ticket.
For the initial version, you can simulate a successful purchase. When adding real payments, issue a valid ticket only after payment is confirmed.

# Flow C — Verify a ticket at the entrance
1. Staff scans the QR code or enters the ticket number.
2. Backend finds the ticket and checks its status.
3. If valid and unused, backend marks it USED.
4. If already used, cancelled, or unknown, backend rejects it.
5. Backend records the verification result.
