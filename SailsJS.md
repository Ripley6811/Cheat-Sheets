##Destroy
    Model.destroy(criteria, function (err, recList) {});
    Model.destroy(criteria).exec(function (err, recList) {});
- `criteria` = Find Criteria	`{},[{}], string, int`
- `function` = Callback
- `recList` = Always returns a list

##Update
    Model.update(criteria, updates, function (err, record) {});
    Model.update(criteria, updates).exec(function (err, record) {});
