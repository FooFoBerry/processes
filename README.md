processes
=========

## Procfile to get processes running

Take this repo and place it in the root path of the meta-project.  For example, your directories could look like:

```
FooFoBerry
|\
| processes/
| costner_goes_postal/
| feed_engine_api/
| feed_engine_auth/
| feed_engine_front_end/
| feed_engine_proxy/
```

Install foreman if you don't have it already

```
gem install foreman
```

Then cd in to the processes directory (`cd processes`) run `foreman start` and all the processes will launch

If you get an error about a port being taken already, run `lsof -i tcp:<port that is taken>` and then go kill that process (`kill -9 <process_id>`).


## Batch update the git repos

To batch update all the repos (`git pull origin master`), from the processes directory run:

```
./git_update
```

You may need to change permissions on the file.  If so, run:

```
chmod a+x git_update
```
