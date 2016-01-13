## Evaluation:

### Koola project

- good job of cleaning and conditioning data
- your CPT dataframe is entirely null values
- an easier way to create indicators of ICD9 codes is using `crosstab`:

```
flat_df = pd.DataFrame(icd2.to_records())
pd.crosstab(foo.RUID, flat_df.ICD9_Code)
```

- the biggest shortcoming of the project is that you only performed one analysis (GB classifier); the project outline targets multiple approaches for comparison. This limits the degree to which you can satisfy some of the criteria for project evaluation.
- though you claim that 500 estimators is sufficient, the score is still growing close to linearly at 500.
- you end up using 100 estimators for your final model. Was this just for expediency, or some other reason?

***IMPORTANT NOTE: please remove the project data from the Github repo (particularly since your project is public). The data should not be shared on the repository***

* introduction of problem, description of methods, discussion of results: 16/20
* runnable by third party: 5/5
* data cleaning and transformation: 10/10
* implementation of methods: 15/25
* cross-validation and model selection: 9/10
* visualization: 6/10
* model checking and comparison: 7/10
* evaluation of performance characteristics: 7/10

***SCORE: 75/100***