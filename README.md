# Installing Helm

Install Helm client
`helm init --client-only`

Install Helm client and Tiller to the current cluster
`helm init`

Install and upgrade Tiller to the current cluster
`helm init --upgrade`

Check the version of Helm installed
`helm version`


# Helm Repositories

List Helm repositories
`helm repo list`

Update list of Helm charts from repositories
`helm repo update`


# Searching Helm Charts

List all installed charts
`helm search`

Search for a chart
`helm search foo`


# Showing Installed Helm Charts

List all installed Helm charts
`helm ls`

List all deleted Helm charts
`helm ls --deleted`

List installed and deleted Helm charts
`helm ls --all`


# Installing/Deleting Helm charts

Inspect the variables in a chart
`helm inspect values stable/mysql`

Install a Helm chart
`helm install --name foo stable/mysql`

Install a Helm chart and override variables
`helm install --name foo --values config.yaml --timeout 300 --wait stable/mysql`

Show status of Helm chart being installed
`helm status foo`

Delete a Helm chart
`helm delete foo`


# Upgrading Helm charts

Return the variables for a release
`helm get values foo`

Upgrade the chart or variables in a release
`helm upgrade --values config.yaml foo stable/mysql`

List release numbers
`helm history foo`

Rollback to a previous release number
`helm rollback foo 1`
