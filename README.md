### Hi there 👋 MongoDB!

```go
// Select is used to determine which fields are displayed or not displayed in the returned results
// Format: bson.M{"age": 1} means that only the age field is displayed
// bson.M{"age": 0} means to display other fields except age
// When _id is not displayed and is set to 0, it will be returned to display
func (q *Query) Select(projection interface{}) QueryI {
	newQ := q
	newQ.project = projection
	return newQ
}
```
