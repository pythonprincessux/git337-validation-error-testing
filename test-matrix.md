# Validation Test Matrix

## Test 1: Empty Submit
**Test values:** All fields left blank  
**Expected result:** Required controls should be recognized by the browser.   
**Observed result:** Submission was blocked. Chrome focused the required Email field and displayed "Please fill out this field." Email and attendance were identified as invalid required controls. The optional date and explanation fields did not receive required field errors.  
**Result:** Pass

## Test 2: Attendance = 0
**Test values:** Email: test@example.com | Attendance: 0  
**Expected result:** Invalid because attendance must be at least 1.  
**Observed result:** Submission was blocked. Chrome displayed "Value must be greater than or equal to 1."  
**Result:** Pass

## Test 3: Attendance = 1
**Test values:** Email: test@example.com | Attendance: 1  
**Expected result:** Allowed required minimum boundary value.  
**Observed result:** The form submitted successfully and the URL query string contained attendance=1.  
**Result:** Pass

## Test 4: Attendance = 8
**Test values:** Email: test@example.com | Attendance: 8  
**Expected result:** Allowed maximum boundary value.  
**Observed result:** I was able to submit the form successfully and the URL query string contained attendance=8.  
**Result:** Pass

## Test 5: Attendance = 9
**Test values:** Email: test@example.com | Attendance: 9  
**Expected result:** Invalid because attendance cannot be above 8.  
**Observed result:** When I entered the value,9, the submission was blocked. Chrome showed "Value must be less than or equal to 8."  
**Result:** Pass

## Test 6: Keyboard Navigation
**Test method:** I navigated through the form using only the Tab key.  
**Expected result:** Controls should have visible focus indicators and follow a logical order as required in assignment instructions.  
**Observed result:** Focus indicator moved through Email, Number attending, Requested date, Short explanation, and Test request in logical order as required by assignment instructions. I also made sure that the disabled Unavailable action button was skipped. Visible focus indicators remained present.  
**Result:** Pass

## Test 7: 320px and 200% Zoom
**Test method:** I tested the form at 320 CSS pixels and 200% zoom.  
**Expected result:** Labels, help, errors, controls, and actions should remain available without overlap.  
**Observed result:** Labels, controls, validation feedback, actions, and server error content remained available and readable. Content reflowed vertically without overlap or horizontal clipping. Had to retest, wasn't testing at 320 and 200 zoom simulataneously. 
**Result:** Pass