# Change Management

## The "Tower Problem"
During a modeling and development life cycle, data model changes and modications are just happening. You might want to add addtional fields that you have missed, or delete an outdated one instead. However, when **applying changes to existing data models can be critical, especially if they have dependencies and impact on other models**. This is true for changes that have been applied on the lower stack of the models and eventually the **modeling "tower" starts to wobble and and become very quickly inconsistent**.

<br><br>![](/exercises/ex0/images/cm_01.png)

Following typical model changes are considered:
- Add / Delete / Rename of a Column
- Add / Delete / Rename of Input Parameter
- Add / Delete Associations
- Share / Unshare Models
- etc.

## Change Management approach in SAP Data Warehouse Cloud
One quick way to stop the **Tower Problem** and inconsistencies is to prohibit and prevent changes and modifications on models with dependencies and impacts on other models.
However, in reality this is not practical. 
1. Strict prevention of inconsistent changes leads very quickly to **modeling inflexiblity**, since changes can not be applied once a model got dependencies to other models. That means, users have to model things from scratch to overcome this strict rule, which is **highly inefficient**.
2. **Changes and modifications can not be always prevented**, e.g. modifications on models in the source system. SAP Data Warehouse Cloud simply has no control over these models and for that can not prohibit such changes, but can only react to them.


For that, SAP Data Warehouse Cloud is following rather the approach of **allowing incompatible changes in a controlled manner**. User may apply compatible as well as incompatible changes, which lead to model inconsitencies and make them no longer runnable during runtime. However, the system shall 
1. provide transparency and detailed information on applied changes
2. provide proposal to resolve issues and potential inconsistencies
3. allow to revert changes (rollback to last consistent state)
4. provide auto refactoring and auto propagation to improve efficiency and reduce manual adjustments


>:mortar_board: In short: **SAP Data Warehouse Cloud allows any kind of changes, while supporting users to resolve the issues and regain a consistent state for the models.**
