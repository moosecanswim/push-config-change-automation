# push-config-change-automation

To get this to work you will need to add a deploy token to your pushing repo:

- click your profile in github then settings > developer settings > personal access tokens
- create a new token with "write:packages" and "repo" and "read:org"
- copy the generated token
- in the pushing repo go to settings > secrets > New repository secret and create a secret "deploy_token" and paste in the generated toke from the last step
- in the github action reference it with `${{ secrets.deploy_token }}.