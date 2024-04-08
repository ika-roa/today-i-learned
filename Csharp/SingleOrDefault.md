# SingleOrDefault() or FirstOrDefault()?
## Important points
### Performance
- `SingleOrDefault()` is potentially slower than `FirstOrDefault()`, as it needs to check all rows, even when it finds a match at the beginning of the table.
- On the other hand, `FirstOrDefault()` will stop looking for rows after finding a row that matches the criteria.
### Error handling
- `SingleOrDefault()` will throw an exception in case there is more than one record matching your criteria found.
- `FirstOrDefault()` will return the first match, even if multiple matches are in the table.