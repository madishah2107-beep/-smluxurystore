# JSONBin.io "Bin cannot be blank" Error - Fix

## ❌ Problem:
"Bin cannot be blank" error aa raha hai even though `[]` hai.

## ✅ Solution:

### **JSON Editor Mein Yeh Likho:**

**Option 1: Empty Object Array (Recommended)**
```json
[{}]
```

**Option 2: Empty Array with Comment**
```json
[]
```

**Option 3: Test Data (Best for Start)**
```json
[{"id":"1","name":"Test"}]
```

---

## 📝 Step-by-Step Fix:

1. **Name field:** `SM_LUXE_STORE` ✅ (already filled)
2. **Collection:** `Uncategorized` ✅ (already selected)
3. **JSON editor:**
   - Clear karo
   - **Yeh type karo:**
   ```json
   [{}]
   ```
   Ya:
   ```json
   []
   ```

4. **"Save Bin"** click karo

---

## ✅ Try These in JSON Editor:

**Option 1 (Recommended):**
```json
[{}]
```

**Option 2:**
```json
[]
```

**Option 3 (If still error):**
```json
{"products":[]}
```

---

## 🔧 If Still Not Working:

1. **Collection field** check karo - kuch select kiya hai?
2. **Name field** check karo - blank to nahi?
3. **JSON editor** mein exactly `[{}]` ya `[]` hai?

---

**Try `[{}]` in JSON editor - yeh usually kaam karta hai!**



