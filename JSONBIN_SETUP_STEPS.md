# JSONBin.io Setup - Step by Step with Screenshots Guide

## 📋 Step-by-Step Instructions

### **Step 1: Create Account**
1. Jao: **https://jsonbin.io/**
2. Top right corner mein **"Sign Up"** ya **"Get Started"** click karo
3. Email se account banao (ya GitHub se)

---

### **Step 2: Create Bin - WHERE TO WRITE NAME?**

#### **Option A: New Bin Button Se**
1. Dashboard par jao
2. **"Create Bin"** ya **"New Bin"** button click karo
3. Ek form/page khulega

#### **Option B: Direct Create**
1. Dashboard par **"+"** icon ya **"Create"** button dikhega
2. Click karo

---

### **Step 3: Bin Creation Form**

Jab bin creation form khulega, aapko yeh dikhega:

```
┌─────────────────────────────────────┐
│  Create New Bin                     │
├─────────────────────────────────────┤
│  Bin Name: [___________]  ← YAHAN  │
│                                     │
│  Data: [___________]                │
│                                     │
│  [Create] [Cancel]                  │
└─────────────────────────────────────┘
```

**"Bin Name"** field mein likho: `SM_LUXE_PRODUCTS` ya `sm-luxe-store`

**"Data"** field mein likho: `[]` (empty array)

---

### **Step 4: Agar Name Field Nahi Dikha**

Agar name field nahi dikha, to:
1. **"Data"** field mein pehle yeh likho:
   ```json
   []
   ```
2. Phir **"Create"** click karo
3. Bin create hone ke baad, bin details page par **"Rename"** option hoga
4. Wahan se name change kar sakte ho

---

### **Step 5: After Creating Bin**

Bin create hone ke baad:

1. **Bin ID** mil jayega - URL mein ya bin page par
   - Example URL: `https://jsonbin.io/app/bins/507f1f77bcf86cd799439011`
   - Bin ID: `507f1f77bcf86cd799439011`

2. **API Key** lein:
   - Top right corner → **Account** → **API Keys**
   - **"Master Key"** copy karo

---

## 🎯 Quick Summary

1. **JSONBin.io** par jao
2. **"Create Bin"** click karo
3. **"Bin Name"** field mein: `SM_LUXE_PRODUCTS` likho
4. **"Data"** field mein: `[]` likho
5. **"Create"** click karo
6. **Bin ID** copy karo
7. **API Key** copy karo
8. `src/cloudStorage.js` file mein paste karo

---

## 📝 Example

**Bin Name:** `SM_LUXE_PRODUCTS`
**Data:** `[]`
**Bin ID:** `507f1f77bcf86cd799439011` (example)
**API Key:** `$2b$10$abc123...` (example)

---

**Agar koi confusion hai, batao - main aur detail dunga!**



