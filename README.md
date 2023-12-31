# content-tools
AEM tools to manage content, such as replicate from on Author to another, or purge content without using a query.

* [activate-tree-extension.zip](activate-tree-extension-2.3.zip) Extension to AEM > Tools > Replication > Activate Tree, where you can specify the replication agent. Useful for transferring content from one Author to another without a package or sending a cache invalidation request directly to the Dispatcher.
* [deleteproperty.zip](deleteproperty-1.0.zip) Remove a property from nodes via traversal or query. Useful for cleaning up unnecessary properties.
* [fix-missing-asset-metadata.zip](fix-missing-asset-metadata-2.0.zip) Traverses a path and finds dam:Asset nodes that are missing the jcr:content/metadata subnodes. If found, it adds the node and runs the specified workflow on it.
* [purge-launches.zip](purge-launches-1.0.zip) Purge launches by walking down the JCR tree starting at /content/launches, looking for cq:Page nodes under /content/launches/YYYY/MM/DD that have liveDate < "now - age" days. If liveDate (Launch Date) does not exist, then it uses jcr:created (the date the launch was created). Does not use a query.
* [purge-workflows.zip](purge-workflows-1.0.zip) Purge completed workflows by walking down the JCR tree starting at /var/workflow/instances, looking for cq:Workflow nodes that have an endTime < "now - age" days. Does not use a query. Useful if the OOTB workflow purge fails due to query traversal limits.
* [unlock-tree.zip](purge-launches-1.3.zip) Traverses a tree of nodes, unlocks both pages and assets that are locked.
