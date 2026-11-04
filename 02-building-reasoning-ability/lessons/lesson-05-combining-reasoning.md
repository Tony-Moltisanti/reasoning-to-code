# Lesson 5: Combining Reasoning Skills

Use this five-step method:
1. **Observe:** What information is available?
2. **Separate:** Which statements are established and which are assumptions?
3. **Connect:** What do the facts actually support?
4. **Test:** Could another explanation fit?
5. **Investigate:** What evidence would resolve uncertainty?

## Clinic appointment example
A screenshot displays a confirmed 10 AM appointment; the current database record says `cancelled`; another patient has a confirmed booking for the slot. These facts do not establish who cancelled the original appointment, when or why. Cancellation history or an audit log is a useful next source of evidence.

## Success message without a saved record
A patient submits a request, the application displays "Booking successful", but no appointment record is created. The supported conclusion is that success was displayed but the booking was not persisted. Investigate the request, server response, database operation and success-message logic.
