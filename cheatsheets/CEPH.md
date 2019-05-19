## Ceph Commands:

### View Status:

```
$ ceph -s
  cluster:
    id:     uuid-x-x-x-x
    health: HEALTH_OK

  services:
    mon: 1 daemons, quorum ceph:10.20.30.40:16789
    mgr: 1f2c207d5ec9(active)
    osd: 3 osds: 3 up, 3 in

  data:
    pools:   2 pools, 200 pgs
    objects: 16  objects, 21 MiB
    usage:   3.0 GiB used, 27 GiB / 30 GiB avail
    pgs:     200 active+clean
```

### List Pools:

```
$ ceph osd lspools
1 default
2 volumes
```

## Get PGNum:

```
$ ceph osd pool get volumes pg_num
pg_num: 100
```

### Set Dashboard Username/Password:

```
ceph dashboard set-login-credentials
```

## Ceph Docker Volumes

### Dockerized Ceph:
- https://github.com/flaviostutz/ceph-osd

### Docker Volume Plugin:
- https://github.com/flaviostutz/cepher

## Resources:
- http://docs.ceph.com/docs/mimic/mgr/dashboard/
- https://wiki.nix-pro.com/view/Ceph_FAQ/Tweaks/Howtos