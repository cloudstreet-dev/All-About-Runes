# Chapter 26: Programming with Runes - UTF-8 and Unicode

## Introduction

Welcome, modern vitki (rune-workers)! In this chapter, we'll explore how to work with runic characters in programming. The Elder Futhark runes are part of the Unicode standard, which means you can use them in virtually any programming language, database, or text file.

## Unicode Basics

### What is Unicode?

Unicode is a universal character encoding standard that assigns a unique code point to every character from every writing system in the world, including the runic alphabets.

### Runic Unicode Block

The Elder Futhark runes are located in the "Runic" Unicode block:
- **Block Range:** U+16A0 to U+16FF
- **Elder Futhark:** U+16A0 to U+16EA
- **Total Runic Characters:** 89 (includes Elder, Younger Futhark, and Anglo-Saxon runes)

## The Elder Futhark Unicode Table

Here's the complete Elder Futhark with Unicode values:

| # | Rune | Name | Unicode | UTF-8 | Decimal |
|---|------|------|---------|-------|---------|
| 1 | ᚠ | Fehu | U+16A0 | E1 9A A0 | 5792 |
| 2 | ᚢ | Uruz | U+16A2 | E1 9A A2 | 5794 |
| 3 | ᚦ | Thurisaz | U+16A6 | E1 9A A6 | 5798 |
| 4 | ᚨ | Ansuz | U+16A8 | E1 9A A8 | 5800 |
| 5 | ᚱ | Raidho | U+16B1 | E1 9A B1 | 5809 |
| 6 | ᚲ | Kenaz | U+16B2 | E1 9A B2 | 5810 |
| 7 | ᚷ | Gebo | U+16B7 | E1 9A B7 | 5815 |
| 8 | ᚹ | Wunjo | U+16B9 | E1 9A B9 | 5817 |
| 9 | ᚺ | Hagalaz | U+16BA | E1 9A BA | 5818 |
| 10 | ᚾ | Nauthiz | U+16BE | E1 9A BE | 5822 |
| 11 | ᛁ | Isa | U+16C1 | E1 9B 81 | 5825 |
| 12 | ᛃ | Jera | U+16C3 | E1 9B 83 | 5827 |
| 13 | ᛇ | Eihwaz | U+16C7 | E1 9B 87 | 5831 |
| 14 | ᛈ | Perthro | U+16C8 | E1 9B 88 | 5832 |
| 15 | ᛉ | Algiz | U+16C9 | E1 9B 89 | 5833 |
| 16 | ᛊ | Sowilo | U+16CA | E1 9B 8A | 5834 |
| 17 | ᛏ | Tiwaz | U+16CF | E1 9B 8F | 5839 |
| 18 | ᛒ | Berkana | U+16D2 | E1 9B 92 | 5842 |
| 19 | ᛖ | Ehwaz | U+16D6 | E1 9B 96 | 5846 |
| 20 | ᛗ | Mannaz | U+16D7 | E1 9B 97 | 5847 |
| 21 | ᛚ | Laguz | U+16DA | E1 9B 9A | 5850 |
| 22 | ᛜ | Ingwaz | U+16DC | E1 9B 9C | 5852 |
| 23 | ᛞ | Dagaz | U+16DE | E1 9B 9E | 5854 |
| 24 | ᛟ | Othala | U+16DF | E1 9B 9F | 5855 |

## Programming Examples

### Python

```python
# Python 3 - Working with Elder Futhark Runes

# Method 1: Using Unicode escape sequences
fehu = '\u16A0'
print(f"Fehu: {fehu}")  # Output: Fehu: ᚠ

# Method 2: Direct entry (if your editor supports it)
uruz = 'ᚢ'
print(f"Uruz: {uruz}")

# Method 3: From code point number
thurisaz = chr(0x16A6)
print(f"Thurisaz: {thurisaz}")  # Output: Thurisaz: ᚦ

# Complete Elder Futhark as list
elder_futhark = [
    '\u16A0',  # Fehu
    '\u16A2',  # Uruz
    '\u16A6',  # Thurisaz
    '\u16A8',  # Ansuz
    '\u16B1',  # Raidho
    '\u16B2',  # Kenaz
    '\u16B7',  # Gebo
    '\u16B9',  # Wunjo
    '\u16BA',  # Hagalaz
    '\u16BE',  # Nauthiz
    '\u16C1',  # Isa
    '\u16C3',  # Jera
    '\u16C7',  # Eihwaz
    '\u16C8',  # Perthro
    '\u16C9',  # Algiz
    '\u16CA',  # Sowilo
    '\u16CF',  # Tiwaz
    '\u16D2',  # Berkana
    '\u16D6',  # Ehwaz
    '\u16D7',  # Mannaz
    '\u16DA',  # Laguz
    '\u16DC',  # Ingwaz
    '\u16DE',  # Dagaz
    '\u16DF',  # Othala
]

# Display all runes
for i, rune in enumerate(elder_futhark, 1):
    code_point = ord(rune)
    print(f"{i:2d}. {rune} - U+{code_point:04X} (decimal: {code_point})")

# Rune dictionary with names
rune_names = {
    '\u16A0': 'Fehu',
    '\u16A2': 'Uruz',
    '\u16A6': 'Thurisaz',
    '\u16A8': 'Ansuz',
    '\u16B1': 'Raidho',
    '\u16B2': 'Kenaz',
    '\u16B7': 'Gebo',
    '\u16B9': 'Wunjo',
    '\u16BA': 'Hagalaz',
    '\u16BE': 'Nauthiz',
    '\u16C1': 'Isa',
    '\u16C3': 'Jera',
    '\u16C7': 'Eihwaz',
    '\u16C8': 'Perthro',
    '\u16C9': 'Algiz',
    '\u16CA': 'Sowilo',
    '\u16CF': 'Tiwaz',
    '\u16D2': 'Berkana',
    '\u16D6': 'Ehwaz',
    '\u16D7': 'Mannaz',
    '\u16DA': 'Laguz',
    '\u16DC': 'Ingwaz',
    '\u16DE': 'Dagaz',
    '\u16DF': 'Othala',
}

# Random rune draw
import random

def draw_rune():
    rune = random.choice(list(rune_names.keys()))
    name = rune_names[rune]
    return f"{rune} - {name}"

print(f"\nRandomly drawn rune: {draw_rune()}")

# Encoding and decoding
text_with_runes = "ᚠᚢᚦᚨᚱᚲ - The first six runes spell 'futhark'"
encoded = text_with_runes.encode('utf-8')
print(f"\nUTF-8 encoded: {encoded}")
decoded = encoded.decode('utf-8')
print(f"Decoded: {decoded}")
```

### JavaScript / Node.js

```javascript
// JavaScript - Working with Elder Futhark Runes

// Method 1: Unicode escape
const fehu = '\u16A0';
console.log(`Fehu: ${fehu}`);  // Output: Fehu: ᚠ

// Method 2: Code point
const uruz = String.fromCodePoint(0x16A2);
console.log(`Uruz: ${uruz}`);  // Output: Uruz: ᚢ

// Elder Futhark array
const elderFuthark = [
    '\u16A0', '\u16A2', '\u16A6', '\u16A8',
    '\u16B1', '\u16B2', '\u16B7', '\u16B9',
    '\u16BA', '\u16BE', '\u16C1', '\u16C3',
    '\u16C7', '\u16C8', '\u16C9', '\u16CA',
    '\u16CF', '\u16D2', '\u16D6', '\u16D7',
    '\u16DA', '\u16DC', '\u16DE', '\u16DF'
];

// Rune class
class Rune {
    constructor(symbol, name, meaning) {
        this.symbol = symbol;
        this.name = name;
        this.meaning = meaning;
        this.codePoint = symbol.codePointAt(0);
    }

    toString() {
        return `${this.symbol} ${this.name} (U+${this.codePoint.toString(16).toUpperCase().padStart(4, '0')})`;
    }

    toJSON() {
        return {
            symbol: this.symbol,
            name: this.name,
            meaning: this.meaning,
            unicode: `U+${this.codePoint.toString(16).toUpperCase().padStart(4, '0')}`,
            decimal: this.codePoint
        };
    }
}

// Example runes
const runes = {
    fehu: new Rune('\u16A0', 'Fehu', 'Wealth'),
    uruz: new Rune('\u16A2', 'Uruz', 'Strength'),
    thurisaz: new Rune('\u16A6', 'Thurisaz', 'Giant'),
};

console.log(runes.fehu.toString());
console.log(JSON.stringify(runes.uruz.toJSON(), null, 2));

// Random rune draw
function drawRune() {
    const rune = elderFuthark[Math.floor(Math.random() * elderFuthark.length)];
    return rune;
}

console.log(`\nRandomly drawn: ${drawRune()}`);
```

### Java

```java
// Java - Working with Elder Futhark Runes

public class RunicExample {
    public static void main(String[] args) {
        // Method 1: Unicode escape
        char fehu = '\u16A0';
        System.out.println("Fehu: " + fehu);

        // Method 2: Code point
        String uruz = new String(Character.toChars(0x16A2));
        System.out.println("Uruz: " + uruz);

        // Elder Futhark array
        String[] elderFuthark = {
            "\u16A0", "\u16A2", "\u16A6", "\u16A8",
            "\u16B1", "\u16B2", "\u16B7", "\u16B9",
            "\u16BA", "\u16BE", "\u16C1", "\u16C3",
            "\u16C7", "\u16C8", "\u16C9", "\u16CA",
            "\u16CF", "\u16D2", "\u16D6", "\u16D7",
            "\u16DA", "\u16DC", "\u16DE", "\u16DF"
        };

        // Display all runes
        for (int i = 0; i < elderFuthark.length; i++) {
            String rune = elderFuthark[i];
            int codePoint = rune.codePointAt(0);
            System.out.printf("%2d. %s - U+%04X (decimal: %d)%n",
                i + 1, rune, codePoint, codePoint);
        }
    }
}
```

### C#

```csharp
// C# - Working with Elder Futhark Runes

using System;
using System.Text;

class RunicExample
{
    static void Main()
    {
        // Method 1: Unicode escape
        char fehu = '\u16A0';
        Console.WriteLine($"Fehu: {fehu}");

        // Method 2: From code point
        string uruz = char.ConvertFromUtf32(0x16A2);
        Console.WriteLine($"Uruz: {uruz}");

        // Elder Futhark array
        string[] elderFuthark = new string[]
        {
            "\u16A0", "\u16A2", "\u16A6", "\u16A8",
            "\u16B1", "\u16B2", "\u16B7", "\u16B9",
            "\u16BA", "\u16BE", "\u16C1", "\u16C3",
            "\u16C7", "\u16C8", "\u16C9", "\u16CA",
            "\u16CF", "\u16D2", "\u16D6", "\u16D7",
            "\u16DA", "\u16DC", "\u16DE", "\u16DF"
        };

        // Display runes
        for (int i = 0; i < elderFuthark.Length; i++)
        {
            string rune = elderFuthark[i];
            int codePoint = char.ConvertToUtf32(rune, 0);
            Console.WriteLine($"{i + 1,2}. {rune} - U+{codePoint:X4} (decimal: {codePoint})");
        }
    }
}
```

### SQL / Databases

```sql
-- SQL - Storing and querying runes in databases

-- Create table with UTF-8 encoding
CREATE TABLE runes (
    id INT PRIMARY KEY,
    symbol NVARCHAR(1),  -- Use NVARCHAR for Unicode
    name VARCHAR(50),
    meaning TEXT,
    unicode_point VARCHAR(10)
) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- Insert Elder Futhark runes
INSERT INTO runes VALUES
(1, 'ᚠ', 'Fehu', 'Wealth and prosperity', 'U+16A0'),
(2, 'ᚢ', 'Uruz', 'Strength and vitality', 'U+16A2'),
(3, 'ᚦ', 'Thurisaz', 'The giant''s gateway', 'U+16A6'),
-- ... (continue for all 24 runes)

-- Query runes
SELECT symbol, name, meaning FROM runes WHERE id = 1;

-- Search by name
SELECT * FROM runes WHERE name LIKE '%Fe%';

-- Random rune draw
SELECT * FROM runes ORDER BY RAND() LIMIT 1;
```

## UTF-8 Encoding Explained

### What is UTF-8?

UTF-8 is a variable-length character encoding that can represent every character in Unicode. Runic characters require 3 bytes in UTF-8.

### Example: Fehu (ᚠ)

- **Unicode code point:** U+16A0
- **UTF-8 encoding:** E1 9A A0 (3 bytes)
- **Binary:** 11100001 10011010 10100000

### Encoding breakdown:
```
U+16A0 = 0001 0110 1010 0000 (binary)

UTF-8 template for 3-byte character:
1110xxxx 10xxxxxx 10xxxxxx

Filling in the bits:
1110[0001] 10[011010] 10[100000]
= E1       9A         A0
```

## Common Issues and Solutions

### Issue 1: Runes Not Displaying

**Problem:** Runes show as boxes or question marks

**Solution:**
- Ensure your font supports runic characters (try "Segoe UI Symbol", "Noto Sans Runic", or "Junicode")
- Verify UTF-8 encoding in your file/database
- Check that your terminal/console supports Unicode

### Issue 2: Database Storage

**Problem:** Runes get corrupted when stored in database

**Solution:**
```sql
-- Use UTF-8 encoding
ALTER DATABASE your_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- Use NVARCHAR or appropriate Unicode type
CREATE TABLE runes (
    symbol NVARCHAR(1)  -- Not VARCHAR
);
```

### Issue 3: Web Display

**Problem:** Runes don't show on webpage

**Solution:**
```html
<!-- Add UTF-8 meta tag -->
<meta charset="UTF-8">

<!-- Use web fonts that support runes -->
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Runic&display=swap" rel="stylesheet">

<style>
    .runic {
        font-family: 'Noto Sans Runic', serif;
        font-size: 24px;
    }
</style>

<p class="runic">ᚠᚢᚦᚨᚱᚲ</p>
```

## Practical Applications

### 1. Rune Casting Simulator

```python
import random

class RuneCast:
    def __init__(self):
        self.runes = [
            ('\u16A0', 'Fehu', 'Wealth'),
            ('\u16A2', 'Uruz', 'Strength'),
            # ... add all 24
        ]

    def draw(self, count=1):
        drawn = random.sample(self.runes, count)
        for symbol, name, meaning in drawn:
            print(f"{symbol} {name}: {meaning}")

caster = RuneCast()
caster.draw(3)  # Draw 3 runes
```

### 2. Runic Message Encoder

```python
def text_to_runes(text):
    """Convert Latin letters to approximate runes"""
    mapping = {
        'f': '\u16A0',  # Fehu
        'u': '\u16A2',  # Uruz
        'th': '\u16A6', # Thurisaz
        'a': '\u16A8',  # Ansuz
        'r': '\u16B1',  # Raidho
        'k': '\u16B2',  # Kenaz
        'g': '\u16B7',  # Gebo
        # ... complete mapping
    }

    result = text.lower()
    # Replace longest matches first
    for key in sorted(mapping.keys(), key=len, reverse=True):
        result = result.replace(key, mapping[key])
    return result

print(text_to_runes("futhark"))  # Output: ᚠᚢᚦᚨᚱᚲ
```

### 3. Rune API

```javascript
// Express.js API for rune information
const express = require('express');
const app = express();

const runeData = [
    { id: 1, symbol: '\u16A0', name: 'Fehu', meaning: 'Wealth' },
    { id: 2, symbol: '\u16A2', name: 'Uruz', meaning: 'Strength' },
    // ... all 24 runes
];

app.get('/api/runes', (req, res) => {
    res.json(runeData);
});

app.get('/api/rune/:id', (req, res) => {
    const rune = runeData.find(r => r.id == req.params.id);
    res.json(rune);
});

app.get('/api/random', (req, res) => {
    const rune = runeData[Math.floor(Math.random() * runeData.length)];
    res.json(rune);
});

app.listen(3000);
```

## Best Practices

1. **Always use UTF-8 encoding** for files and databases
2. **Test your font** supports runic characters
3. **Use Unicode escape sequences** for portability (\u16A0 rather than direct entry)
4. **Validate input** if accepting user-generated runic content
5. **Document encoding** in your code comments

## Resources

- **Unicode Standard:** https://unicode.org/charts/PDF/U16A0.pdf
- **Runic Fonts:**
  - Junicode: https://junicode.sourceforge.io/
  - Noto Sans Runic: https://fonts.google.com/noto/specimen/Noto+Sans+Runic
- **Testing:** https://unicode-table.com/en/blocks/runic/

*Why do programmers love runes? Because they're the original character encoding!*

---

**Previous:** [Chapter 25 - Othala (ᛟ)](./25-othala.md) | **Next:** [Appendix: Quick Reference Guide](./27-quick-reference.md)
