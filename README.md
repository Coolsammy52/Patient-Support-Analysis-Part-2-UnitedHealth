# Patient-Support-Analysis-Part-2-UnitedHealth
Patient Support Analysis (Part 2) [UnitedHealth

SELECT 
  ROUND (100.0 *
    COUNT(case_id)  filter (
      WHERE call_category is NULL OR call_category = 'n/a')
      / COUNT(case_id), 1) AS uncategoriesed_call_pct
FROM callers;
