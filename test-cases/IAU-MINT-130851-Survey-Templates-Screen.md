# IAU | MINT | شاشة عرض قوالب الاستبيانات (Survey Templates Screen)

**User Story ID:** 130851  
**Module:** الاستبيانات (Questionnaires)  
**Screen Name:** قوالب الاستبيانات (Survey Templates)

**Total Test Cases:** 95

---

## 1. Page Load & Display

1. Check that 'قوالب الاستبيانات' screen loads within 3 seconds and displays correct title and breadcrumb navigation.
2. Check that the screen is responsive on desktop, tablet, and mobile with proper RTL direction.
3. Check that the screen displays correctly in both light and dark modes.

---

## 2. Create Button: إنشاء قالب استبيان جديد

4. Check that the button 'إنشاء قالب استبيان جديد' is visible only to users with create permission.
5. Check that clicking 'إنشاء قالب استبيان جديد' navigates to the create form without errors or page refresh.

---

## 3. Search Field: عنوان الاستبيان

6. Check that the search field accepts text input and displays placeholder text.
7. Check that searching with exact or partial survey title returns matching templates.
8. Check that searching with non-existent title displays 'لا توجد نتائج مطابقة لمعايير البحث.'.
9. Check that searching handles whitespace, special characters, and long input correctly.
10. Check that search results update in real-time and pagination resets to page 1.

---

## 4. Filter: الوحدة المرتبطة (Associated Module)

11. Check that the filter 'الوحدة المرتبطة' displays all available modules with 'الكل' option and allows multiple selections.
12. Check that selecting one or multiple modules displays only templates linked to those modules.
13. Check that selecting 'الكل' displays templates from all modules.
14. Check that filter state is maintained when other filters are applied and resets on page refresh.

---

## 5. Filter: المرحلة المرتبطة (Associated Stage)

15. Check that the filter 'المرحلة المرتبطة' displays all available stages with 'الكل' option and allows multiple selections.
16. Check that selecting one or multiple stages displays only templates linked to those stages.
17. Check that combining 'المرحلة المرتبطة' with 'الوحدة المرتبطة' returns templates matching both criteria.

---

## 6. Filter: حالة الاستبيان (Survey Status)

18. Check that the filter 'حالة الاستبيان' shows 'مفعل', 'غير مفعل', and 'الكل' options.
19. Check that selecting 'مفعل' displays only active templates and 'غير مفعل' displays only inactive templates.
20. Check that selecting both statuses displays all templates.

---

## 7. Combined Filters & Reset

21. Check that applying two or more filters simultaneously returns accurate results.
22. Check that a 'Clear All Filters' button is available when filters are applied and clears all filters.
23. Check that clearing one filter maintains other active filters.

---

## 8. Template Cards - Display & Layout

24. Check that template cards display in a consistent grid/list layout with proper spacing.
25. Check that cards are responsive and no visual overlap occurs.
26. Check that long titles are truncated with ellipsis and full text appears in tooltip on hover.

---

## 9. Template Cards - Content Display

27. Check that each card displays 'عنوان الاستبيان' as main heading, 'الوحدة المرتبطة', 'المرحلة المرتبطة', and 'حالة الاستبيان' accurately.
28. Check that status 'مفعل' and 'غير مفعل' are visually distinct with different colors.
29. Check that templates without associated stage do not display stage field.

---

## 10. Empty States

30. Check that message 'لا توجد قوالب استبيانات متاحة.' displays when no templates exist.
31. Check that message 'لا توجد نتائج مطابقة لمعايير البحث.' displays when no templates match search/filter criteria.

---

## 11. Action: عرض تفاصيل القالب (View Template Details)

32. Check that 'عرض تفاصيل القالب' button is visible on each card and according to permissions.
33. Check that clicking the card or 'عرض تفاصيل القالب' navigates to template details screen with correct data.

---

## 12. Action: تعديل القالب (Edit Template)

34. Check that 'تعديل القالب' button is visible only with edit permission.
35. Check that clicking 'تعديل القالب' navigates to edit form pre-populated with template data.
36. Check that changes are saved and template list refreshes after successful edit.

---

## 13. Action: معاينة القالب (Preview Template)

37. Check that 'معاينة القالب' button is visible according to permissions.
38. Check that clicking 'معاينة القالب' opens preview showing all questions without edit options.

---

## 14. Action: تفعيل القالب (Activate Template)

39. Check that 'تفعيل القالب' button appears only for inactive templates and is visible with activate permission.
40. Check that clicking 'تفعيل القالب' displays confirmation dialog with exact message 'هل أنت متأكد من تفعيل قالب الاستبيان؟'.
41. Check that clicking 'نعم' activates template, updates status to 'مفعل', replaces button with 'إلغاء تفعيل القالب', and refreshes list.
42. Check that clicking 'إلغاء' closes dialog without activating template.

---

## 15. Action: إلغاء تفعيل القالب (Deactivate Template)

43. Check that 'إلغاء تفعيل القالب' button appears only for active templates and is visible with deactivate permission.
44. Check that clicking 'إلغاء تفعيل القالب' displays confirmation dialog with exact message 'هل أنت متأكد من إلغاء تفعيل قالب الاستبيان؟'.
45. Check that clicking 'نعم' deactivates template, updates status to 'غير مفعل', and replaces button with 'تفعيل القالب'.
46. Check that deactivated template is prevented from new operations but existing surveys remain unaffected.

---

## 16. Action: حذف القالب (Delete Template)

47. Check that 'حذف القالب' button is visible only with delete permission.
48. Check that clicking 'حذف القالب' displays confirmation dialog with exact message 'هل أنت متأكد من حذف قالب الاستبيان؟'.
49. Check that clicking 'نعم' deletes template, removes it from list, and refreshes display.
50. Check that attempting to delete a template already used displays error 'لا يمكن حذف قالب الاستبيان لأنه سبق استخدامه.' and prevents deletion.

---

## 17. Pagination

51. Check that pagination controls display when templates exceed page limit.
52. Check that 'Next' button is enabled/disabled appropriately and 'Previous' button is disabled on first page.
53. Check that clicking 'Next', 'Previous', or page number navigates to correct page and loads within 2 seconds.
54. Check that pagination resets to page 1 when search or filters are applied.

---

## 18. Default Sorting

55. Check that templates are sorted by default from newest to oldest (descending creation date).
56. Check that sorting order is maintained with search and filters applied.
57. Check that a sorting toggle allows changing to ascending order and current direction is visually indicated.

---

## 19. Template Ownership & Sharing

58. Check that templates created by current user and templates shared with user are both displayed.
59. Check that only templates with proper permissions are visible.
60. Check that shared templates are clearly identified and user can perform permitted actions on them.

---

## 20. Template Data Persistence

61. Check that active and inactive template data, questions, and structure are fully preserved.
62. Check that deactivating and reactivating template preserves all data.
63. Check that edited template changes are saved and linked associations (module, stage) are updated.

---

## 21. Success Messages

64. Check that success messages display after creating, editing, activating, deactivating, and deleting templates.

---

## 22. Error Handling

65. Check that error messages display for creation, editing, activation, deactivation, and deletion failures.
66. Check that network and timeout errors display with user option to retry.
67. Check that validation errors display for required fields that are empty.

---

## 23. Permissions & Access Control

68. Check that 'إنشاء قالب استبيان جديد' button is visible only with create permission.
69. Check that 'تعديل القالب' action is visible only with edit permission.
70. Check that 'عرض تفاصيل القالب' action is visible only with view permission.
71. Check that 'تفعيل القالب' and 'إلغاء تفعيل القالب' are visible only with activate permission.
72. Check that 'حذف القالب' action is visible only with delete permission.
73. Check that 'معاينة القالب' action is visible only with preview permission.
74. Check that attempting to access actions without permission via direct URL shows error or redirects.

---

## 24. Performance

75. Check that initial page load completes within 3 seconds even with 100+ templates.
76. Check that search results display within 2 seconds and do not freeze UI.
77. Check that filter results display within 2 seconds and multiple filters do not significantly slow performance.
78. Check that action buttons (edit, delete) respond within 1 second and complete within 5 seconds.

---

## 25. Browser Compatibility

79. Check that screen displays and functions correctly in Chrome with no console errors.
80. Check that screen displays and functions correctly in Microsoft Edge with no console errors.

---

## 26. Responsive Design

81. Check that screen is responsive on desktop (1920x1080), tablet (768x1024), and mobile (320x480).
82. Check that elements do not overflow or misalign on smaller screens and all interactive elements are accessible on touch devices.

---

## 27. Language Support

83. Check that all Arabic labels, buttons, and messages display correctly with proper RTL direction.
84. Check that switching to English displays interface correctly with LTR direction and accurate translations.
85. Check that mixed Arabic and English content displays correctly with proper text direction handling.

---

## 28. Accessibility

86. Check that all interactive elements are accessible via keyboard (Tab navigates, Enter activates).
87. Check that focus state is clearly visible throughout navigation.
88. Check that screen readers announce screen title, button labels, and filter options correctly.
89. Check that confirmation dialogs are announced correctly by screen readers.
90. Check that text has sufficient color contrast and status indicators are distinguishable.

---

## 29. Data Consistency & Integrity

91. Check that displayed survey title, module, stage, and status match system data.
92. Check that after editing/activating/deactivating/deleting templates, changes reflect immediately in list.
93. Check that if a module or stage is deleted, linked templates are handled correctly.

---

## 30. UI & Confirmation Dialog Behavior

94. Check that confirmation dialogs display as modal overlays with dimmed background, centered position, and functional 'نعم' and 'إلغاء' buttons.
95. Check that clicking outside dialog (if applicable) does not close it and confirmation message clearly indicates action consequences.

---

## Notes for QA Team

- All Arabic UI terms preserved exactly as specified.
- Test cases cover functional, UI, validation, data, workflow, security, and performance aspects.
- Execute tests across Chrome, Edge on desktop, tablet, and mobile.
- Run permission-based tests with different user roles.
- Perform regression tests after each release.

---

**Document Version:** 2.0 (Condensed)  
**Date Created:** October 2026
