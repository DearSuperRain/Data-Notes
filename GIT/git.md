#git�ٲ��


Git�ڶ�ֻ������״̬�����޸ģ�modified�������ݴ棨staged�������ύ��committed�������޸ı�ʾ�޸���ĳ���ļ�������û���ύ���棻���ݴ��ʾ�����޸ĵ��ļ������´��ύʱҪ������嵥�У����ύ��ʾ���ļ��Ѿ�����ȫ�ر����ڱ������ݿ����ˡ�

��Ӧ������������Git �Ĺ���Ŀ¼���ݴ������Լ����زֿ⡣

��ν���ݴ�����ֻ�����Ǹ��򵥵��ļ���һ�㶼���� Git Ŀ¼�С���ʱ�����ǻ������ļ����������ļ���������׼˵�����ǽ��ݴ�����	

������ Git �����������£�
1. �ڹ���Ŀ¼���޸�ĳЩ�ļ���
1. ���޸ĺ���ļ����п��գ�Ȼ�󱣴浽�ݴ�����
1. �ύ���£����������ݴ�������ļ���������ת���� Git Ŀ¼�С�

���ǿ��Դ��ļ�������λ�����ж�״̬�������GitĿ¼�б����ŵ��ض��汾�ļ������������ύ״̬����������޸Ĳ��ѷ����ݴ����򣬾��������ݴ�״̬��������ϴ�ȡ���������޸ĵ���û�зŵ��ݴ����򣬾������޸�״̬��

``` bash
#����ȫ�ֵ��û���������
$ git config --global user.name waile23
$ git config --global user.email waile23@163.com

#�����汾��
$ git clone <url> #��¡Զ�̰汾��
$ git init #��ʼ�����ذ汾��

#�޸ĺ��ύ
$ git status #�鿴״̬
$ git diff #�鿴�������
$ git add . #���������޸ĵ��ļ����浽�ݴ������ļ���Ϊ���ݴ�
$ git add <file> #��ָ�������޸ĵ��ļ����浽�ݴ������ļ���Ϊ���ݴ� 
$ git add -u #�������Ѿ��޸ĵ��ļ����浽�ݴ������ļ���Ϊ���ݴ�
$ git commit -m ��commit message�� #�ύ���ݴ��ļ�
$ git commit --amend #�޸����һ���ύ
$ git rm <file> #ȡ��git���ļ��İ汾����.
$ git rm --cached <file> #ȡ��git���ļ��İ汾���ƣ�-�Ccachedѡ����������ļ���������Ĺ���Ŀ¼��.�����ã�
$ git mv <old> <new> #�������ļ�����ɾ�����ļ�����������ļ������������ã���

#��־
$ git log --oneline --stat #�鿴��־�����Բ鿴�ļ��б� ��ʾÿ�θ��µ��޸��ļ���ͳ����Ϣ
$ git log -p #��������ʾÿ�����¼�Ĳ���

#����������

$ git checkout HEAD <file> #����ָ����δ�ύ(���޸ģ����ݴ�)�ļ����޸����ݣ�����֤����Ŀ¼�е�״̬�����ύ״̬һ�¡�
$ git revert <commit> #�ع���ָ�����ύ(��ûŪ����)

$ git reset HEAD <file> #ȡ�����ݴ���ļ�������������ǰ"git add"�Ĳ�����
$ git reset --hard HEAD #�ѹ���Ŀ¼������δ�ύ(���޸ģ����ݴ�)���������(��Ȼ�ⲻ����δ���ڰ�����µ��ļ� untracked files)��
$ git reset --hard <commit_id>(��ϣֵ��ǰ�����ַ�)���׻��˵�ĳ���汾�����ص�Դ��Ҳ���Ϊ�ð汾�����ݡ�

���ݨCsoft �Cmixed �Chard�����working tree��index��HEAD��������:
    git reset �Cmixed����ΪĬ�Ϸ�ʽ�������κβ�����git reset����ʱ���ַ�ʽ�������˵�ĳ���汾��ֻ����Դ�룬����commit��index��Ϣ
    git reset �Csoft�����˵�ĳ���汾��ֻ������commit����Ϣ������ָ���index fileһ���������Ҫ�ύ��ֱ��commit����
    git reset �Chard�����׻��˵�ĳ���汾�����ص�Դ��Ҳ���Ϊ��һ���汾������
    
���ɣ� $ git reset --hard <commit_id> �� git push origin HEAD --force ���ã����׻��˵�ĳ���汾���ύ��������ɾ��ָ���汾�����ύ��������ʹ�ø÷���ɾ�������ύ��

#��֧���ǩ
$ git branch #��ʾ���б��ط�֧
$ git branch <new-branch> #�����·�֧  
$ git checkout <branch/tag> #�л���ָ����֧���ǩ  
$ git checkout -b <branch/tag> #�൱��$ git branch <branch/tag>   $git checkout <branch/tag>  
$ git branch -d <branch> #ɾ�����ط�֧
$ git tag #�г����б��ر�ǩ
$ git tag <tagname> #���������ύ������ǩ
$ git tag -d <tagname> #ɾ����ǩ

#�ϲ����ܺ�
$ git merge <branch> #�ϲ�ָ����֧����ǰ��֧���µİ汾
$ git rebase <branch> #�ܺ�ָ����֧����ǰ��֧���γ�����

#merge����������һ���µĽڵ㣬֮ǰ���ύ�ֿ���ʾ����rebase�������������µĽڵ㣬�ǽ�������֧�ںϳ�һ�����Ե��ύ��
#��Ҫ���õ��ύ����ʹ��rebase���������һ�㡣
#Զ�̲���

$ git remote -v #�鿴Զ�̰汾����Ϣ
$ git remote show <remote> #�鿴ָ��Զ�̰汾����Ϣ
$ git remote add <remote> <url> #���Զ�̰汾��
$ git fetch <remote> #��Զ�̿��ȡ����
$ git pull <remote> <branch> #���ش��뼰���ٺϲ�
$ git pull <remote> <branch>:<local-branch>  ȡ��remote��branch��֧���뱾�ص�local-branch��֧�ϲ�,ע��ð�ź����пո�  
$ git push <remote> <branch> #�ϴ����뼰���ٺϲ�
$ git push <remote> :<branch/tag-name> #ɾ��Զ�̷�֧���ǩ
$ git push --tags #�ϴ����б�ǩ


#����ssh key
ssh-keygen -t rsa -C "����"  #����ssh key��Ȼ�������ʾ�����س�������~/.sshĿ¼�µõ�id_rsa��id_rsa.pub�����ļ���id_rsa.pub�ļ����ŵľ�������Ҫʹ�õ�key��
ssh -T git@github.com #�����Ƿ����óɹ�
```

##�ο�

[��Դ](https://gitcafe.com/GitCafe/Help/wiki/Git-%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4%E9%80%9F%E6%9F%A5%E8%A1%A8#wiki)

http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html

http://www.ituring.com.cn/article/202419

http://www.cnblogs.com/renkangke/archive/2013/05/31/conquerAndroid.html
