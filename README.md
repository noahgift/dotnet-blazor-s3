# dotnet-blazor-s3

## Install dotnet

```
sudo yum -y update
sudo yum -y install libunwind
```

```
wget https://dot.net/v1/dotnet-install.sh
chmod +x dotnet-install.sh 
sudo ./dotnet-install.sh -c Current
```


Change `~/.bashrc`
```
export PATH="$PATH:$HOME/.local/bin:$HOME/bin:$HOME/.dotnet:$HOME/.rvm/bin"
export DOTNET_ROOT=$HOME/.dotnet
```

Verify it works:

```
dotnet --version
```

Create Blazor App

```
dotnet new blazorserver -o BlazorApp --no-https
```

Install the AWS .NET Core deploy tool:

```
dotnet tool install -g aws.deploy.tools
```
Add to path
```
export PATH="$PATH:/home/ec2-user/.dotnet/tools"
```

Verify it works.

```
dotnet aws deploy --help
```


## References

* [Install dotnet](https://docs.aws.amazon.com/cloud9/latest/user-guide/sample-dotnetcore.html)
