# 🧪 Monefy App Bug Report

This document lists a series of identified bugs in the Monefy Android app, based on thorough testing conducted on a Samsung A35 device. All bugs are verified on Android OS.

## 📋 Summary of Issues

| Title | Steps to Reproduce | Evidence | Environment | Severity | Priority | Impact | Mode |
|-------|---------------------|----------|-------------|----------|----------|--------|------|
| Currency change updates payment icons but not monetary values | - Open Monefy app<br>- Add payment entries using USD<br>- Go to currency settings<br>- Change from USD to Euro<br>- Return to home<br>- Icons change, but values stay the same | Video | Android<br>Device: Samsung A35 | High | High | Values mismatch across currencies; false financial insight | Online |
| App crashes when returning to home after changing date interval | - Open app with payments from 26–29<br>- Change interval to 20–31<br>- Return to home screen | Video | Android<br>Device: Samsung A35 | High | High | App crash forces restart; usability blocked | Online |
| Budget mode alerts not functioning | - Enable budget mode<br>- Set limit: 50,000<br>- Spend above 50,000<br>- No alerts shown | Video | Android<br>Device: Samsung A35 | Medium | Medium | No alert for exceeding budget; feature fails | Online |
| Tutorial popup persists across pages | - First-time launch or clear data<br>- Observe tutorial popup<br>- Navigate between pages<br>- Popup doesn't disappear | Video | Android<br>Device: Samsung A35 | Medium | Medium | Disrupts navigation for new users | Online |
| Donut chart shows incorrect percentages | - Add >5 category-based payments<br>- Check donut chart in various intervals<br>- Percentages and colors mismatch<br>- Some categories missing | Attachments | Android<br>Device: Samsung A35 | High | Medium | Misleading analytics and visuals | Online |
| Incomplete language translation | - Change app language in settings<br>- Navigate across app<br>- Some text stays in original language | Video | Android<br>Device: Samsung A35 | Low | Medium | Mixed-language UI; poor localization | Online |
| Calculator allows incomplete expressions | - Try “3+”, “6+3+”, etc.<br>- Calculator shows result instead of error | Video | Android<br>Device: Samsung A35 | Medium | Medium | Wrong calculations accepted; incorrect entries saved | Online |
| Income/Expense buttons show symbols instead of text | - On home screen, check action buttons<br>- "+" and "-" shown instead of "Income" / "Expense" | Attachments | Android<br>Device: Samsung A35 | Low | Medium | Symbolic buttons cause confusion | Online |

---
