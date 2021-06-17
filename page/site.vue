<style>
.mdui-card-header { height: 36px; }
.mdui-card-header-avatar { height: auto;}
</style>
<template>
    <div class="mdui-card-content mdui-typo">
        <div class="mdui-row-xs-1 mdui-row-sm-2 mdui-row-md-4">
            <a v-for="site in sites" :key="site.title" :href="site.url" :title="site.desc" target="_blank" class="mdui-col mdui-m-b-1">
                <div class="mdui-card mdui-hoverable">
                    <div class="mdui-card-header">
                        <i class="mdui-icon material-icons mdui-card-header-avatar mdui-typo-title mdui-text-color-green">cloud</i>
                        <div class="mdui-card-header-title mdui-text-truncate">{{site.title}}</div>
                    </div>
                    <div class="mdui-card-content mdui-text-truncate">
                        {{site.desc}}
                    </div>
                </div>
            </a>
        </div>
    </div>
</template>
<script>
    Rap.define("",[],{
        data: function(){
            return {
                sites:[
                    { title:"Steam上的中文Galgame",url:"https://steamgalgame.com",desc:"致力于收集Steam上的中文Galgame，方便大家快速查找和获取Steam上最新的官方中文Galgame。"},
                    { title:"萝卜の图站",url:"https://img.ijglb.com",desc:"个人ACG图片收集站，随缘更新。"},
                    { title:"☀️阳向心美 / 陽向ここみ / Hinata Cocomi💜",url:"https://cocomi.ijglb.com",desc:"Vtuber‘阳向心美’的应援网站。"},
                    { title:"博客备份",url:"https://blogbak.ijglb.com",desc:"以前的博客网站，仅作保留，不再更新。"},
                ]
            }
        },
        init:function () {
            this.$emit('update:ptitle', "我的站点");
        }
    })
</script>
