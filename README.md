# Priority Rendering (react-concurrency)

## useTransition

**useTransition()** tells React that some state updates have a lower priority,, i.e., every other state updates or UI rendering trigger has a higher priority. When we call useTransition(), we get an array with exactly two elements: an isPending boolean value that indicates if the low-priority state update is still pending, and a startTransition() function that you can wrap around a state update to tell React that it’s a low-priority update.

## useDefferedValue

**useDeferredValue()** does the same thing as useTransition(), making a slow and laggy interface faster. However, it is used in a slightly different way. According to React team member Dan Abramov, useDeferredValue() is mainly

"useful when the value comes “from above” and you don’t actually have control over the corresponding setState call."