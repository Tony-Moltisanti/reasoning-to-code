# Lesson 7 — Modal Language in Requirements

Words such as `can`, `must`, `shall`, `should`, `may` and `will` affect the strength and meaning of requirements. Their exact meanings can vary by organisation and document convention, so specifications should define them where precision matters.

| Word | Common meaning | How to interpret it |
|---|---|---|
| `can` | Ability or sometimes permission | Describes capability or possibility; context matters |
| `must` | Requirement or obligation | Strong mandatory language |
| `shall` | Often a formal requirement or obligation | Commonly used for a binding specification requirement; check the document's convention |
| `should` | Recommendation or expected good practice | Usually weaker than `must` |
| `may` | Permission or possibility | Often grants permission; does not guarantee the action occurs |
| `will` | Future action, intention or expected behaviour | Often describes an expected outcome; convention may vary |

## Must versus should

- “The patient must be logged in to book” states a mandatory condition.
- “The patient should receive a confirmation message” usually states a recommendation or expected good practice, unless the specification defines `should` differently.

Do not silently turn a recommendation into an absolute requirement or a mandatory rule into an optional one.

## Can versus may

- “The patient can cancel” may describe capability or permission.
- “The patient may cancel” often grants permission, but can express possibility in ordinary language.

Neither statement proves that cancellation has already happened.

## Shall versus will

- “The system shall record the booking” commonly states a formal requirement.
- “The system will record the booking” commonly describes expected future behaviour or intention.

Some organisations use these terms differently. Follow the specification's definitions.

## Modal words and conditional logic

“The patient must be logged in and may book if verified or approved by an administrator.”

A reasonable interpretation:

- Login is mandatory.
- Verification or administrator approval provides an allowed route.
- “May book” grants permission under the rule; it does not guarantee that the patient will actually book.

A permission is not the same as a completed action.
