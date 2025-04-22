created >= -7d
Explanation:
This query retrieves all issues that were created in the past 7 days, including today. The -7d means "7 days ago from today."

b) Issues created in the last 30 days
created >= -30d


c) Issues created more than 90 days ago
created <= -90d

2. Find Issues Resolved Between Specific Dates
a) Issues resolved between January 1, 2024, and March 31, 2024
resolved >= "2024-01-01" AND resolved <= "2024-03-31"

b) Issues resolved in the previous quarter (relative to today)
resolved >= startOfQuarter(-1) AND resolved <= endOfQuarter(-1)

c) Issues resolved in the current year
resolved >= startOfYear()

Bonus Challenge
Issues created in the last 30 days and resolved within 7 days of creation
created >= -30d AND resolutionDate <= created +7d

Created in the last 30 days
And resolved within 7 days after their creation date
