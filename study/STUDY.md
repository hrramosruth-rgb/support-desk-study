# MERN support-ticket flow — source study

These notes were added in October 2026. The application is the work of the original upstream contributors. This fork does not claim the upstream code, dates, or experience as work by Ruth Ramos.

Source: [bradtraversy/support-desk](https://github.com/bradtraversy/support-desk). The exact imported revision is recorded in [SOURCE.json](SOURCE.json).

## Source map

| Entry point | What to trace |
| --- | --- |
| [backend/server.js](../backend/server.js) | Express application entry |
| [backend/middleware/authMiddleware.js](../backend/middleware/authMiddleware.js) | Bearer-token verification and current-user loading |
| [backend/controllers/ticketController.js](../backend/controllers/ticketController.js) | Ticket list, create, read, update, and delete handlers |
| [frontend/src/features/tickets/ticketSlice.js](../frontend/src/features/tickets/ticketSlice.js) | Ticket state and request actions |
| [frontend/src/pages/Ticket.jsx](../frontend/src/pages/Ticket.jsx) | Single-ticket interface |

## Study exercise

The reviewed ticket list filters by the current user; creation assigns that user on the server. Follow the update handler separately and review its permitted fields before extending it. A useful future regression would check that an update cannot change ticket ownership.

## Setup and verification

Use the preserved [upstream README](../readme.md) for setup and the repository package scripts for the exact commands. This addition changes documentation only. Dependencies were not installed and application tests were not run.

The added documentation was checked for valid local links, a matching upstream revision, unchanged application files, and preservation of the [MIT license](../MIT-LICENSE.txt).

## Attribution

The original license and copyright notice remain unchanged. All imported commits retain their original authors. Only this fork's study documentation is a new contribution dated October 2026.
