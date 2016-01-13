
#### Usage


If you installed with `npm`, this module will be in your `node_modules` folder, so the command is: 

```
  node node_modules/simple-cfn-wait/index \
    --stack <STACK_NAME> \
    --interval <SECONDS_PING> \
    --max <MAX_TIMES>
```

Make sure you have `AWS_PROFILE` set to a profile that allows you to `DescribeStacks` on the Stack that you are waiting for, and `AWS_REGION` is set to the correct region for the stack.

`--interval` and `--max` are optional. They represent the time between polls to cloudformation to use in seconds and the maximum amount of times to check the stack, respectively. They will default to 60 seconds and 10 times.