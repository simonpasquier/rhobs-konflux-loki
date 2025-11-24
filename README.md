# rhobs-konflux-loki

Use this repository to deploy Loki and Loki operator built with Konflux for RHOBS.next.

## Update submodule

1. Go to https://gitlab.cee.redhat.com/openshift-logging/konflux-log-storage/ (midstream repository of the Logging product) and select the release branch you want to upgrade to. Write down the branches for the Loki and Loki operator submodules. Pay attention that the branches may be different!
2. Update the branch name in the `.gitmodules` file and checkout the required commit in the `loki` directory.
3. Repeat the same operation for the [Loki operator](https://github.com/rhobs/rhobs-konflux-loki-operator).

Update the submodule to the latest commit:
```bash
cd path/to/submodule
git fetch --tags
git checkout tag_name
cd ..
git add path/to/submodule
git commit -m "Updated submodule to tag_name"
git push
```
