Seeing if/how GitHub can support the CI-friendly 'safe merging of changes to main' workflow detailed here:

http://rickardlindberg.me/writing/what-should-a-ci-server-do/#basic-workflow

Summary of the desired server behaviour:

The integration server triggers on a commit to a branch, then clones the repo, merges origin/branch locally into main, and executes the test/deploy pipeline on the local main. If whatever we've defined as a pipeline is successful, it pushes the result of the merge back to origin/main. As a result, main is always fully validated as working.

Run tests with `npm test`
