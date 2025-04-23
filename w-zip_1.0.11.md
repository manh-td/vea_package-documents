w-zipA compression tool with zip and 7z.DocumentationTo view documentation or get support, visitdocs.InstallationUsing npm(ES6 module):Note:w-zipis mainly dependent onarchiver,archiver-zip-encryptedandunzipper.Note:If you want to use7zon windows, you need to install7zon your computer first.npm i w-zipExample for ZIP:Link:[dev source code]import wz from 'w-zip'

let fpUnzip = './testData/outputZip'
let fpUnzipExtract = fpUnzip + '/extract'

let fpSrc1 = './testData/input/file1(ä¸­æ).txt'
let fpZip1 = fpUnzip + '/test1.zip'

let fpSrc2 = './testData/input/folder1'
let fpZip2 = fpUnzip + '/test2.zip'
let fpZip2PW = fpUnzip + '/test2PW.zip'
let pw = 'abc'

async function test() {

    //zipFile
    console.log('zipFile before')
    console.log('zipFile', await wz.mZip.zipFile(fpSrc1, fpZip1))
    console.log('zipFile after')

    //zipFolder
    console.log('zipFolder before')
    console.log('zipFolder', await wz.mZip.zipFolder(fpSrc2, fpZip2))
    console.log('zipFolder after')

    //zipFolder with password
    console.log('zipFolder with password before')
    console.log('zipFolder with password', await wz.mZip.zipFolder(fpSrc2, fpZip2PW, { pw }))
    console.log('zipFolder with password after')

    //unzip
    console.log('unzip1 before')
    console.log('unzip1', await wz.mZip.unzip(fpZip1, fpUnzipExtract + '/test1'))
    console.log('unzip1 after')

    //unzip
    console.log('unzip2 before')
    console.log('unzip2', await wz.mZip.unzip(fpZip2, fpUnzipExtract + '/test2'))
    console.log('unzip2 after')

    //unzip with password
    console.log('unzip2 with password before')
    console.log('unzip2 with password', await wz.mZip.unzip(fpZip2PW, fpUnzipExtract + '/test2PW', { pw }))
    console.log('unzip2 with password after')

}
test()
    .catch((err) => {
        console.log(err)
    })

// zipFile before
// zipFile done: ./testData/outputZip/test1.zip
// zipFile after
// zipFolder before
// zipFolder done: ./testData/outputZip/test2.zip
// zipFolder after
// zipFolder with password before
// zipFolder with password done: ./testData/outputZip/test2PW.zip
// zipFolder with password after
// unzip1 before
// unzip1 done: ./testData/outputZip/extract/test1
// unzip1 after
// unzip2 before
// unzip2 done: ./testData/outputZip/extract/test2
// unzip2 after
// unzip2 with password before
// unzip2 with password done: ./testData/outputZip/extract/test2PW
// unzip2 with password afterExample for 7z:Link:[dev source code]import wz from 'w-zip'

let fpUnzip = './testData/output7z'
let fpUnzipExtract = fpUnzip + '/extract'

let fpSrc1 = './testData/input/file1(ä¸­æ).txt'
let fpZip1 = fpUnzip + '/test1.7z'

let fpSrc2 = './testData/input/folder1'
let fpZip2 = fpUnzip + '/test2.7z'
let fpZip2PW = fpUnzip + '/test2PW.7z'
let pw = 'abc'

async function test() {

    // //setProg
    // let path7zexe = 'path of 7zEXE'
    // wz.m7z.setProg(path7zexe)

    //zipFile
    console.log('zipFile before')
    console.log('zipFile', await wz.m7z.zipFile(fpSrc1, fpZip1))
    console.log('zipFile after')

    //zipFolder
    console.log('zipFolder before')
    console.log('zipFolder', await wz.m7z.zipFolder(fpSrc2, fpZip2))
    console.log('zipFolder after')

    //zipFolder with password
    console.log('zipFolder with password before')
    console.log('zipFolder with password', await wz.m7z.zipFolder(fpSrc2, fpZip2PW, { pw }))
    console.log('zipFolder with password after')

    //unzip
    console.log('unzip1 before')
    console.log('unzip1', await wz.m7z.unzip(fpZip1, fpUnzipExtract + '/test1'))
    console.log('unzip1 after')

    //unzip
    console.log('unzip2 before')
    console.log('unzip2', await wz.m7z.unzip(fpZip2, fpUnzipExtract + '/test2'))
    console.log('unzip2 after')

    //unzip with password
    console.log('unzip2 with password before')
    console.log('unzip2 with password', await wz.m7z.unzip(fpZip2PW, fpUnzipExtract + '/test2PW', { pw }))
    console.log('unzip2 with password after')

}
test()
    .catch((err) => {
        console.log(err)
    })
    
// zipFile before
// zipFile finish: ./testData/output7z/test1.7z
// zipFile after
// zipFolder before
// zipFolder finish: ./testData/output7z/test2.7z
// zipFolder after
// zipFolder with password before
// zipFolder with password finish: ./testData/output7z/test2PW.7z
// zipFolder with password after
// unzip1 before
// unzip1 finish: ./testData/output7z/extract/test1
// unzip1 after
// unzip2 before
// unzip2 finish: ./testData/output7z/extract/test2
// unzip2 after
// unzip2 with password before
// unzip2 with password finish: ./testData/output7z/extract/test2PW
// unzip2 with password after