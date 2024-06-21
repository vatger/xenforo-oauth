# Xenforo-OAuth

The Xenforo OAuth plugin allows the use of the VATSIM Germany's OAuth2 provider with the [Xenforo](https://xenforo.com/) forum software. 

> [!NOTE]
> Although the Addon is tailored towards the VATSIM Germany OAuth2 implementation, VATSIM's implementation can (with minor modifications) be used as well. 

## Contact

|         Name         | Responsible for |     Contact     |
|:--------------------:|:---------------:|:---------------:|
| Nikolas G. - 1373921 |        *        | `git@vatger.de` |
|  Paul H. - 1450775   |        *        | `git@vatger.de` |

## Prerequisites
You are going to need a (local) instance of Xenforo. The respective documentation on where to obtain the source code can be found here: https://xenforo.com/docs/dev/.
After that, extract the contents of this repository into `/src/addons`, which should leave you with the following structure: `/src/addons/VATGER/OAuth/...`. 

## Installing and Running
### Installing
You can use Xenforo's CLI to install the addon using 
```shell
$ php cmd.php xf:addon-install VATGER/OAuth
``` 

> [!CAUTION]
> Make sure to create a backup of the database beforehand as the installation will alter the `xf_user` table.

### Configuration
Within the Xenforo CP, navigate to `Setup > Options > VATGER - OAuth`. Here you'll be greeted with the following (empty) page:

<img src="./docs/img/xenforo_settings.png" width="700px" alt="Xenforo settings page">

Once you've entered your data in these fields, OAuth should simply work! The "Log in" button on the homepage is overridden to navigate to `/oauth` which starts the flow and signs the user in. 