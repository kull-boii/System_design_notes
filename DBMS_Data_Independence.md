## Logical data independence
The ability to change the conceptual schema without changing the external schema or user view is called logical data independence. For example, the addition or removal of new entities, attributes or relationships to this conceptual schema should be possible without having to change existing external schemas or rewriting existing application programs.

In other words, changes to the conceptual schema (e.g., alterations to the structure of the database, like adding a column or other tables) should not affect the function of the application (external views).

## Does data independence work in reality?
Generally, physical data independence exists in most databases and file environments where physical details, such as the exact location of data on disk or the type of storage device, are hidden from the user. On the other hand, logical data independence is harder to achieve because it must accommodate changes in the structure of the database without affecting application programs; which is a much stricter requirement.
