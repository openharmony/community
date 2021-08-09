# SIG Management Regulations
English | [简体中文](./README.md)

## Background
Under the guidance of the Project Management Committee (PMC), a special interest group (SIG) designs the architecture, develops open capabilities, and performs maintenance for innovative projects in a specific domain.
This repository stores information about all the SIGs in the OpenHamony community.

## Applying for Creating an SIG
1. Seek two or three developers in the community who have the same interest or objectives as you and elect a leader for this SIG. Create an SIG proposal based on the [SIG creation template](sig-template/oep_cn.md) (this template is based on the [KEP template](https://github.com/kubernetes/enhancements/blob/master/keps/NNNN-kep-template/README.md)).
2. The SIG leader sends the SIG proposal via an email with the title [New-SIG-Proposal-XXX] to dev@openharmony.io.
3. Wait for the PMC to approve the proposal, after which the leader can create an SIG.

## Joining an SIG
Find an SIG you are interested in and participate in its technical discussions, maintenance, and capability development by various means, such as subscribing to mailing lists and attending meetings of the SIG.

## Operating and Maintaining an SIG
1. The SIG leader forks the **OpenHamony/community** release, creates a folder and names it with the SIG name in the **sig** directory, creates an SIG profile in the created folder based on the [SIG template](sig-template/), and submits pull requests (PRs) for incorporating modifications of the SIG profile into the master code of OpenHarmony.
2. SIG incubation projects are stored in the [OpenHarmony-SIG](https://gitee.com/openharmony-sig) organization. The code of incubation projects that meet graduation requirements can be incorporated into the master code of OpenHarmony.
3. The SIG leader and committer operate and maintain the SIG.
4. The SIG leader periodically reports the progresses of the SIG operations and incubation projects to the PMC which then offers suggestions.

## Graduation of SIG Incubation Projects
1. If your SIG incubation project meets graduation requirements, you can apply for incorporating its code into the master code of OpenHarmony.
2. The SIG leader sends a graduation application for the incubation project to dev@openharmony.io.
3. After the PMC approves the graduation application, you can incorporate the code of the incubation project into the master code of OpenHarmony.

### How SIG Data Is Stored and Managed
SIG data is stored in the **sig** directory of the **OpenHamony/community** repository. The **sig_***xxx***.md**/**sig_***xxx***_cn.md** file is a template that contains the objectives and work scope of this SIG, repositories managed by the SIG and their descriptions, and SIG meetings and members. A backup of the maintainer/committer information of the SIG is stored in the **OWNER** file and can be automatically obtained by a tool. The names and directory structures of the repositories managed by each SIG are stored in the **sigs.json** file.
1. The **sigs.json** file in the **sig** directory of the **OpenHarmony/community** repository is used to manage all the SIGs visible to the PMC.
2. The PMC modifies and maintains SIGs. Maintainers submit PRs for modifying SIGs, and the PMC reviews the PRs and incorporates the modifications into the master code of OpenHarmony.
3. The **sig_***xxx***.md**/**sig_***xxx***_cn.md** file in the **sig** directory stores SIG data. In this file, the basic SIG information is empty and needs to be specified during SIG creation.
4. The **OWNER** file in the **sig** directory stores information about the maintainer of the SIG.


###  sigs.json File
| Field | Description |
|:---|:---|
|  sig-name | SIG name |
|  projects| Gitee repository name |
|  project-path | Archive path of the OpenHarmony project. Enter **NONE** if the code of the SIG does not need to be incorporated into the master code of OpenHarmony. |

### sigs.json Sample
```
"sigs-List":[
      {
         "sig-name":"sig-python",
         "projects":"https://gitee.com/openharmony-sig/python",
         "project-path":"python/"
      },
      {
         "sig-name ":"sig-updates",
         "projects":["https://gitee.com/openharmony/startup_appspawn_lite", "https://gitee.com/openharmony/startup_bootstrap_lite"]
         "project-path":["base/startup/appspawn_lite", "base/startup/bootstrap_lite"]
      },
   ]
}
```
