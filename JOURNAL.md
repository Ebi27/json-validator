# JSON VALIDATOR PROJECT


    # My personal learning map
            learning_map = {
                "start": {
                    "problem": "Parse {}",
                    "solution": "Exact string match",
                    "next_challenge": "One key-value pair"
                },
                "key_value": {
                    "problem": "Parse {'key': 'value'}",
                    "discovered": "Need to find colon position",
                    "solution": "String scanning",
                    "next_challenge": "Multiple key-value pairs"
                },

            }


## Phase 1: Basic JSON PARSER

**Goal:** Create a basic JSON parser that can validate simple JSON structures.
*Note: Start so small, it is impossible to fail. Start messy, start slow, start unsure... just start!*

**Features to Build:**

1. **Add Simple CLI Interface:**


2. **Core Parser:** Validate if a file contains a valid JSON

     - [ ] Setup project environment.
     - [ ] Write basic Script that parses an empty object.
     - [ ] Validate string quotes: "key": "value".
     - [ ] Check for basic data types: strings, numbers, booleans, null.
     - [ ] Handle escape sequences.


3. **Error Messages:** Give helpful error messages

     - [ ] Missing closing brace.
     - [ ] Strings must use double quotes.
     - [ ] Missing comma between elements.

**Topics to Cover;**

   - [ ] Basic programming concepts (variables, functions, conditionals).
   - [ ] CLI interface basics.
   - [ ] Simple file operations.
   - [ ] Unit Testing.
   - [ ] Basic JSON structure understanding

**Success Criteria:**
   - [ ] Can validate at least 5 different valid JSON strings.
   - [ ] Can identify 3 common JSON syntax errors.
   - [ ] Runs from command line with clear feedback.


## Messy Journal

### Day 1: Discovering the Need for Position Tracking
**Problem:** Kept losing place in string
**Failed approach:** Tried to use split(':') - broke on nested colons
**Solution:** Added `pos` variable to track position
**Aha moment:** "Oh, I need to move through the string character by character!"

### Day 3: Discovering Stacks
**Problem:** Nested objects {{}} confused my parser
**Failed approach:** Tried counting braces - lost track of which object I was in
**Solution:** Used list as stack to push/pop object contexts
**Aha moment:** "The last opened object should be the first closed!"
